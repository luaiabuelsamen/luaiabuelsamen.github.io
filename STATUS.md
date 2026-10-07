Goal: Every project card on the site is accurate and every number traces to a committed results file.
Finish line: Honesty pass committed locally (Rocket, cuRobo, two-hand/DexTrack attribution, new mpc_parking + vega_curobo cards); Luai approves push.
Deadline: 2026-10-31
Milestone: Tier 2 item 1: honesty pass, committed and not pushed
Last result: mpc_parking card: 13/13 stress cases, 0 collisions, 0 deadline misses (mpc_parking/artifacts/benchmark.json); 6/6 traffic cases (mpc_parking/artifacts/traffic_benchmark.json). Two-hand card: 3.2–8.8 mm reference penetration over 9 clips (opposition-deficit/results/dextrack_audit/reference_penetration.json).
Blocked: needs Luai approval to push the about.md honesty pass. Also needs Luai's call on numbers that trace only to prose, not to a results file: humanoid getup "189 to 868" (humanoid_getup/WRITEUP.md; 868 is a peak eval), geometric-learning 1e-8/1e-2/0.13 vs 18.6 (no local repo), UKF "rank 2/40".
Next: none until Luai decides (closer moves on to filter-cost).
Updated: 2026-10-06 20:42

## Changes
- Rocket: removed "real-time performance" (HANDOFF/README: ~150 s cold solve) and "environmental constraints" (point mass, no aero); now describes the constraints SCvx actually enforces.
- cuRobo: removed "real-time" and "significant speedups" (no comparison exists; curobo_berkeley only has its own planning-time stats).
- Two-hand retargeting: credits DexTrack (Liu et al.) for the policy, task and references; dropped the 19 mm figure (it appears only in a code comment).
- New mpc_parking card (numbers listed above) and new vega_curobo card with no numbers: the compliance A/B ran with actuator limits off (vega_curobo/vega_curobo/scene.py:159, ctrlrange ±1e6), and 8.7 mm / 0.26 mm appear only in the README.
- GUFIC_mujoco appears only as the credited source of the vega_curobo control law (Seo et al.).
