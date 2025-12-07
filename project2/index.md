
---

## 6️⃣ `project2/index.md` – Final Robot (Project Assignment 2)

This will be your **main final project page** (four-bar / grasshopper leg, etc.).

```markdown
---
layout: default
title: "Project Assignment 2 – Final Robot"
---

# Project Assignment 2 – Final Robot

This page documents my final project for the Foldable Robotics course:  
a **foldable robot based on a four-bar mechanism**, simulated in MuJoCo and built as a laminated physical prototype.

---

## 🎯 Goals

- Build a **dynamic MuJoCo model** of the robot with:
  - Material compliance (hinges, beams)
  - Actuator / motor behavior
- Choose at least one **design parameter** (e.g., stiffness, link length) and:
  - Sweep it over a range
  - Optimize it for a performance metric (e.g., jump height, speed, distance, efficiency)
- **Fabricate** a laminated version of the mechanism.
- **Compare** simulated predictions against real-world experiments.

---

## 1. System Model (MuJoCo)

- Final geometry and link dimensions.
- Joint stiffness / flexure properties.
- Servo / motor modeling (torque limits, speed, control rules).
- Sites and sensors added to track:
  - Position / velocity
  - Jump height or distance
  - Energies, etc.

If you have a screenshot of the MuJoCo model:

```markdown
![MuJoCo model](./media/mujoco_model.png)
