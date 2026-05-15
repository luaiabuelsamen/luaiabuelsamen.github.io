---
title: "RVT for LeRobot (WIP)"
excerpt: "Bringing multi-view transformer policies (RVT) into Hugging Face's LeRobot ecosystem — MuJoCo SO-ARM100 with 4 RGBD cameras, PerAct/RLBench-format data pipeline, and a LeRobot-compatible policy wrapper.<br/><img src='/images/rvt_lerobot_pipeline.png'>"
collection: portfolio
---

**Status:** Work in progress · [code](https://github.com/luaiabuelsamen) (private repo, ping me for access)

LeRobot ships ACT, Diffusion Policy, VQ-BeT, π0, SmolVLA — all RGB-only,
dense-action policies. There is no 3D / keyframe-based policy in the family.
[RVT](https://github.com/NVlabs/RVT) (Robotic View Transformer, CoRL 2023) is
the canonical one. This project is a minimal bridge: a MuJoCo SO-ARM100 env
with 4 RGBD cameras, a PerAct/RLBench-format data dumper, and a
LeRobot-compatible policy wrapper around RVT.

![pipeline](/images/rvt_lerobot_pipeline.png)

## How the multi-view transformer actually works

The view projection is **not learned**. It is a deterministic geometric step:

1. **RGBD from 4 real cameras** (front, left/right shoulder, wrist) — each pixel
   carries an `(R, G, B, depth)` value plus the camera's intrinsics and extrinsics.
2. **Unproject + fuse** — each camera's depth map is lifted into 3D, points are
   transformed into a single world-frame point cloud (≈60k points here).
3. **Re-render from 5 fixed orthographic virtual cameras** (front, top, left,
   right, back), z-buffered.
4. **Transformer** — patchify each virtual view, add view-id embeddings, cross-view
   attention. Language goal tokenized and concatenated.
5. **Action head** — per-pixel heatmap on each virtual view → highest-scoring
   3D point is the next end-effector keypose. Rotation and gripper-open are
   auxiliary heads.

RVT predicts the *next keyframe*, not a continuous action — which is also why
inference is much cheaper than e.g. ACT or Diffusion Policy at deploy time.

## What's built so far

| Component | Status |
|---|---|
| MuJoCo SO-ARM100 env with 4 RGBD cameras + intrinsics/extrinsics export | ✅ |
| PerAct/RLBench on-disk format writer (depth as 24-bit RGB-packed PNG) | ✅ |
| Keyframe extractor (gripper-state transitions + low-velocity points) | ✅ |
| Scripted demo collector | ✅ (open-loop; needs IK for reliable picks) |
| PCD fusion + 5-view orthographic re-renderer | ✅ |
| Interactive 3D viewer via [rerun](https://rerun.io) | ✅ |
| LeRobot `PreTrainedPolicy`-shaped wrapper | 🚧 stub with explicit integration TODOs |
| Real RVT training run on the new dataset | 🚧 next |
| Upstream PR to `huggingface/lerobot` | 🚧 the goal |

## The "hero" view

A single MuJoCo step, four real RGBD cameras on top, the same scene reprojected
from five orthographic virtual cameras on the bottom — the transformer only ever
sees the bottom row.

![virtual views hero](/images/rvt_lerobot_hero.png)

## Stack

`MuJoCo` · `gymnasium` · `PyTorch` · `rerun` · `PerAct/RLBench format` · `LeRobot` · `RVT (NVlabs)`

## Why this is useful

- **Format bridge** — LeRobot's HF-dataset format and RLBench's episode format
  serve different paradigms. Going both directions cleanly is a real plumbing gap.
- **3D policy in LeRobot** — opens the door to PerAct, RVT, RVT-2, and other
  voxel/PCD-conditioned methods that LeRobot can't currently host.
- **Keyframe inference** — RVT's one-shot-per-keypose inference is dramatically
  cheaper than action-chunking policies; a useful complement when latency matters.

*Last updated: May 2026.*
