---
title: "Go2 Quadruped Locomotion — Sim-to-Sim PPO Fine-tuning"
excerpt: "Fine-tuned the walk-these-ways Go2 policy from Isaac Gym to MuJoCo with PPO and the full CoRL gait-shaping reward.<br/><img src='/images/go2_trot.gif'>"
collection: portfolio
---

![Go2 trotting in MuJoCo](/images/go2_trot.gif)

The pretrained [walk-these-ways](https://github.com/Improbable-AI/walk-these-ways) Go2 policy was trained in Isaac Gym (PhysX) and falls within ~2 seconds when transferred to MuJoCo due to physics discrepancies. To close the sim-to-sim gap I fine-tuned the actor with PPO directly inside MuJoCo on a Jetson Orin NX.

**Approach**

- Reused the upstream `ActorCritic`, `PPO`, and `RolloutStorage` classes from `walk-these-ways-go2/go2_gym_learn/ppo_cse` to keep the model architecture, adaptive-KL learning-rate scheduler, and rollout machinery identical to the original training setup.
- Froze the adaptation module — without privileged observations in MuJoCo the PPO adaptation loss would have collapsed it to predict zeros and destroyed the latent the actor relies on.
- Ported the full CoRL reward (18 terms) into the MuJoCo env: `tracking_lin_vel`, `tracking_ang_vel`, gait-shaped contact-force and contact-velocity rewards, `raibert_heuristic`, `feet_clearance_cmd_linear`, `orientation_control`, `collision`, `feet_slip`, `action_smoothness_1/2`, joint-space penalties, and the ji22-style multiplicative gating `r = pos · exp(neg / σ)`.
- Wrote a per-step gait clock with von-Mises smoothed `desired_contact_states` (κ = 0.07) so the contact-shaping rewards have a target gait pattern matching the trot the policy was pretrained on.

**Result**

After ~4.5M PPO steps with 32 parallel MuJoCo environments (~90 min on the Jetson), the policy holds full 500-step episodes at the velocity command shown above and trots cleanly across the command space.

Code: [`luaiabuelsamen/Go2_locomotion`](https://github.com/luaiabuelsamen/Go2_locomotion)
