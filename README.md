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
