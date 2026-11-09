# EE5110 Grasping Lab

A self-contained visualization of MuJoCo/Panda robotic grasping experiments.

## View locally

Open index.html in a browser. No server, Python environment or internet is required.

## Included

- Three real MuJoCo H.264 replays with synchronized contact-force telemetry.
- Four-strategy comparison, 120 recorded development episodes, and per-object counts.
- Interactive timeline, episode inspection, CSV/JSON export and A/B/C task status.

The HTML replays recorded simulations; it does not run new robot physics in the browser.
Results concern three known YCB objects and a controlled one-shot initial-state bias.
They are development results, not a held-out or real-robot evaluation.

## GitHub Pages

Publish from the main branch, root folder, via Settings > Pages.

## Attribution

YCB Object and Model Set: Berk Calli, Arjun Singh, Aaron Walsman, Siddhartha Srinivasa,
Pieter Abbeel and Aaron M. Dollar. Dataset: CC BY 4.0.
https://ycb-benchmarks.s3.amazonaws.com/index.html

Panda model: Google DeepMind MuJoCo Menagerie, Apache-2.0.
https://github.com/google-deepmind/mujoco_menagerie/tree/main/franka_emika_panda

MuJoCo simulation: https://mujoco.org/

## Independent final evaluation

Live dashboard: https://jackeysz.github.io/ee5110-grasping-lab/

Frozen implementation, reserved seeds 100-199, 500 recorded final episodes:

| Group | Task successes | Program errors | Timeouts (retained failures) |
|---|---:|---:|---:|
| Stale initial state / single | 30/100 | 0 | 0 |
| Stale initial state / retry | 34/100 | 0 | 0 |
| Stale initial state / replan | 64/100 | 0 | 0 |
| Stale initial state / contact recovery | 88/100 | 0 | 4 |
| Clean state / full single-attempt pipeline | 93/100 | 0 | 0 |

Every stale group had the same 30/100 first-attempt successes. Recovery resolved
58/70 initial failures. Paired with replan: both succeed 60, contact only 28,
replan only 4, both fail 8. Nominal Wilson 95% interval for contact recovery:
80.2%-93.0%. Frozen-source integrity verified; no final-result-driven retuning.

Held out: random placements and bias directions. The identities remain the
same three known objects. Re-observation uses perfect simulator geometry;
this is not a claim about unseen objects, persistent vision noise or real robots.
The dashboard separates development records from final evaluation and provides
export of all 500 final rows. No failed or timed-out trial was removed.
