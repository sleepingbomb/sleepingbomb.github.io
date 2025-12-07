---
layout: default
title: "System Model (MuJoCo)"
parent: "Project 2 – Final Robot"
nav_order: 1
---

# System Model (MuJoCo)

This section corresponds to **Part 1: Define the System Model** of the assignment.

## 🎯 Goal

Create a **final dynamic MuJoCo model** that adapts:

- The ideal kinematics from the proposal (Project 1)
- To the **final geometry**, **material properties**, and **actuator behavior**

## 📐 Model Details

Describe:

- **Geometry**: link lengths, four-bar layout, body dimensions.
- **Joints & Compliance**:
  - Hinge stiffness
  - Beam/flexure stiffness
- **Actuators / Motors**:
  - Servo selection and torque/speed
  - How actuation is modeled in MuJoCo (e.g., position control, torque control)

You might link to files like:

- MuJoCo XML: `project2/models/final_robot.xml`
- Jupyter notebook: `project2/notebooks/system_model.ipynb`

## 🎥 Visuals

Add images or screenshots:

```markdown
![MuJoCo model of the robot](./media/mujoco_model.png)
