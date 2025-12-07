---
layout: default
title: "Project 2 – Final Robot"
nav_order: 3
has_children: true
---

# Project 2 – Final Robot

This project documents my final robot for the Foldable Robotics course:
a foldable, grasshopper-inspired robot based on a four-bar mechanism, modeled in MuJoCo and built as a laminated prototype.

The structure of this section follows the assignment:

1. [System Model (MuJoCo)](system-model.html) – final dynamic model, geometry, and joint definitions.
2. [Design Optimization](optimization.html) – parameter sweeps and optimization of key design variables.
3. [Manufacturing Plan & Execution](manufacturing.html) – materials, fabrication steps, and assembly process.
4. [Experimental Validation](experimental-validation.html) – comparing simulation predictions against the real robot.
5. [Report & Video](report-and-video.html) – final written report and presentation video.

---

## Table of contents

- [System Model (MuJoCo)](system-model.html)
- [Design Optimization](optimization.html)
- [Manufacturing Plan & Execution](manufacturing.html)
- [Experimental Validation](experimental-validation.html)
- [Report & Video](report-and-video.html)

---

## Quick overview

- **Concept:**  
  A foldable, grasshopper-style leg built as a four-bar linkage with compliant joints that store and release energy.

- **Simulation (System Model):**  
  A MuJoCo model that captures the link lengths, masses, hinge stiffness, and actuator behavior used in the real robot.

- **Design Optimization:**  
  Design parameters (e.g., hinge stiffness, leg length, mass distribution) are varied in simulation to improve performance
  metrics such as **jump height**, **distance traveled**, and **energy efficiency**.

- **Manufacturing Plan & Execution:**  
  The final mechanism is realized as a laminated structure (e.g., paper/cardboard/PLA layers), including:
  - Cutting patterns and DXFs  
  - Lamination and folding steps  
  - Assembly order for joints, servos, and rubber bands/flexures

- **Experimental Validation:**  
  Physical experiments repeat the same parameter changes tested in simulation and measure:
  - Jump height / distance  
  - Repeatability across trials  
  - Where the sim-to-real gap appears (e.g., friction, backlash, material non-idealities)

- **Report & Video:**  
  A final notebook-based report and a short video summarize:
  - The modeling and optimization pipeline  
  - The manufacturing process  
  - The best robot configuration and its performance

Each of the links above takes you to a dedicated page with figures, notebooks, CAD files, and videos so that someone else can understand, reproduce, or extend this robot design.


