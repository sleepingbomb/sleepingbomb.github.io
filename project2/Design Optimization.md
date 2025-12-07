---
layout: default
title: "Design Optimization"
parent: "Project 2 – Final Robot"
nav_order: 2
---


# Design Optimization

This section corresponds to **Part 2: Optimize Your Design**.

## 🎯 Goal

Select one or more **design parameters** and study how they affect performance.  
Example parameters:

- Hinge stiffness
- Leg length or mounting position
- Mass distribution

## 📏 Performance Metric

Define the metric you used, e.g.:

- Maximum jump height
- Distance traveled in one hop
- Energy efficiency (height per joule)

Explain **why you chose this metric** and how it relates to real experiments.

## 🧪 Parameter Sweep

- Regenerate the MuJoCo model (XML) programmatically for each parameter value.
- Run simulations and collect metrics.
- Plot **performance vs. design variable**.

```markdown
![Performance vs stiffness](./media/performance_vs_stiffness.png)
