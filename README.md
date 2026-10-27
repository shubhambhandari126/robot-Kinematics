# Robot Arm Studio

An interactive robot-arm kinematics playground that runs entirely in the browser — no robot, no install, no dependencies.

**Live demo:** _(add your URL after deploying)_

## What it does

Visualizes the two directions of robot motion:

- **Forward Kinematics (FK)** — you set each joint angle with sliders; the hand ends up wherever that puts it.
- **Inverse Kinematics (IK)** — you drag a target; the arm solves what every joint must do to reach it (using the **FABRIK** algorithm).

Plus the things that separate a sim from a toy:
- **Pick & place task** — grab a block and carry it to a goal zone (the core warehouse-robot job)
- **Joint limits** — each joint can't bend past ±120°, like a real motor
- **Obstacle** — a no-go zone the target can't enter
- **Trajectory tracing** — the hand follows a path (how robots weld or draw)
- Live readouts: hand position, reach used, solve iterations, reachable status
- Adjustable degrees of freedom (2–8 joints) and segment length

## Tech

Plain HTML + Canvas + JavaScript. The IK solver is FABRIK (Forward And Backward Reaching Inverse Kinematics). One self-contained file (`index.html`), ~19 KB, zero external libraries.

## Run it

Just open `index.html` in any browser, or deploy the folder to any static host (GitHub Pages, Netlify, Vercel).

---

Built as the capstone of a 30-day Robotics AI learning project.
