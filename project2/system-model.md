---
layout: default
title: "System Model (MuJoCo)"
parent: "Project 2 – Final Robot"
nav_order: 1
---

# System Model (MuJoCo)

This section corresponds to **Part 1: Define the System Model** of the assignment.

## Goal

Create a **final dynamic MuJoCo model** that adapts:

- The ideal kinematics from the proposal (Project 1)  
- To the **final geometry**, **material properties**, and **actuator behavior** of the robot  

## Model Details

Describe (and link to) your actual model files here:

- **Geometry**  
  - Link lengths, four-bar layout, body dimensions  
  - Any assumptions or simplifications (2D vs 3D, symmetry, etc.)

- **Joints & Compliance**  
  - Hinge stiffness values  
  - Beam/flexure stiffness  
  - Where compliance is modeled in MuJoCo (joint stiffness, tendons, etc.)

- **Actuators / Motors**  
  - Servo model and key specs (torque, speed, gear ratio)  
  - How actuation is modeled (position control, torque control, motor limits)

You might link to files like:

- `project2/models/final_robot.xml`  
- `project2/notebooks/system_model.ipynb`  

## Visuals

Add images or screenshots to make the model easier to understand, for example:

```markdown
![MuJoCo model of the robot](./media/mujoco_model.png)
