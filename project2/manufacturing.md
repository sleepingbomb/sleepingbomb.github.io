
---
layout: default
title: "Manufacturing"
parent: "Project 2 – Final Robot"
nav_order: 3
---

# Manufacturing Plan & Execution

This page documents **how the final robot was physically built** – from material choices and layer design to lamination, cutting, and assembly.  
The goal is that another student could **rebuild the same robot** using only this page plus the provided DXFs/CAD files.

---

## 1. Design & Manufacturing Overview

The final robot is a **foldable, grasshopper-inspired leg** based on a **four-bar mechanism**:

- Laminated layers form the rigid links (ground, rocker links, and coupler).
- Thin flexure regions or hinge cutouts act as compliant joints.
- A servo motor drives one of the links to compress and release the mechanism, generating hopping motion.

The manufacturing strategy is:

1. **Laser-cut / print** the link and hinge patterns from flat sheets.
2. **Laminate** layers to achieve the required stiffness and thickness.
3. **Assemble** the four-bar mechanism with alignment pins/bolts.
4. **Attach** the servo and any rubber bands/flexures.
5. **Tune** clearances and stiffness to match the MuJoCo model.

---

## 2. Materials & Tools

### 2.1 Materials

Adjust these bullet points to match your actual build:

- **Structural layers**
  - e.g., 1–2 mm cardboard or card stock for quick prototypes  
  - or 3 mm acrylic / laser plywood / 3D-printed PLA for final version
- **Flexible / hinge layers**
  - e.g., thinner paper, PET sheet, or Kapton for flexure joints
- **Adhesives**
  - Spray adhesive / glue stick / double-sided tape for lamination
- **Fasteners**
  - M2/M3 screws, nuts, and spacers
  - Paper clips or pins (for low-fidelity prototypes)
- **Actuation**
  - Servo motor (e.g., SG90 / MG90S / MG996R – update with your real one)
  - Servo horn and mounting screws
- **Extras (if used)**
  - Rubber bands for extra “spring” behavior
  - Small weights / washers for tuning mass distribution

### 2.2 Tools

- Laser cutter or craft cutter (for DXFs)
- Scissors / hobby knife (for manual cutting or trimming)
- Ruler / calipers (for checking dimensions and thickness)
- Screwdriver set for servo and fasteners
- Cutting mat and clamps / weights for lamination

---

## 3. Layer Design & DXF Files

All manufacturing files for this robot are organized as:

- `DXF` / `SVG` files for:
  - **Ground link**
  - **Two rocker links**
  - **Coupler link**
  - **Base / mounting plate for the servo**
- Optional:
  - **Drill templates** for servo mounting holes
  - **Flexure pattern** for compliant hinges

> **Download Links (update these to your real paths):**
> - [`links_ground_rockers_coupler.dxf`](../assets/dxf/links_ground_rockers_coupler.dxf)
> - [`servo_mount_plate.dxf`](../assets/dxf/servo_mount_plate.dxf)
> - [`flexure_pattern.dxf`](../assets/dxf/flexure_pattern.dxf)

### 3.1 Link Geometry

The link lengths and pivot positions are chosen to match the MuJoCo model in the **System Model (MuJoCo)** page:

- Ground link length: *[fill in value]* mm
- Rocker link length: *[fill in value]* mm
- Coupler link length: *[fill in value]* mm
- Hinge locations: centered on the laser-cut holes / flexure lines

If you change any of these dimensions in CAD, make sure to **update both**:

1. The **DXF files** (for manufacturing), and  
2. The **MuJoCo XML** (for simulation).

---

## 4. Lamination Process

1. **Print / cut each layer:**
   - Export the patterns from CAD as DXF/SVG.
   - Load them into the laser cutter software and cut on the chosen material.
2. **Label parts:**
   - Immediately label each link (e.g., “Ground”, “Rocker A”, “Rocker B”, “Coupler”) to avoid confusion.
3. **Stack layers:**
   - For rigid links, stack *N* layers until the overall thickness matches the model.
   - Example: three layers of 1 mm card stock → 3 mm effective thickness.
4. **Apply adhesive:**
   - Use spray adhesive or double-sided tape between layers.
   - Start from one side and press out air bubbles.
5. **Press & cure:**
   - Place the laminated stack under books / a flat weight for 10–20 minutes.
   - Ensure the edges stay aligned while curing.

> **Tip:**  
> For flexure joints, **do not laminate** across the hinge region. Leave a thin, flexible layer at the hinge line so it can bend repeatedly.

---

## 5. Assembly Steps

### 5.1 Prepare the Hinges

- For **pin joints**:
  - Use a laser-cut hole (e.g., 3 mm) and insert an M3 screw with nut and spacer.
- For **flexure joints**:
  - Leave a narrow neck or thin region in the material.
  - Verify that it bends freely through the required range of motion.

### 5.2 Assemble the Four-Bar

1. **Attach Rocker A** to the ground link at the first pivot.
2. **Attach Rocker B** to the ground link at the second pivot.
3. **Attach the coupler** between the distal ends of Rocker A and Rocker B.
4. Verify that:
   - The four-bar can **fully fold and unfold** without binding.
   - The coupler follows the intended path (compare with your simulation).

Add washers/spacers between layers if links rub against each other.

### 5.3 Mount the Servo

1. Fix the servo to the **base / ground link** using the mounting plate:
   - Align the servo shaft with the intended joint in the four-bar.
2. Attach the **servo horn** to one rocker link:
   - Center the servo (send it to its neutral angle in code).
   - Align the mechanism in the “neutral” position.
   - Screw the horn to the link or directly clamp/glue it to the rocker.
3. Gently move the mechanism through its range of motion by hand to ensure:
   - No collisions
   - No overextension of flexures
   - Servo torque is sufficient to compress the mechanism

### 5.4 Add Rubber Bands / Extra Springs (if used)

- Hook rubber bands between:
  - The coupler and the ground, or
  - Between the two rocker links
- Tune the pretension:
  - More pretension → higher stored energy, but higher load on the servo.
  - Match the effective stiffness with the value used in the MuJoCo model.

---

## 6. Execution: From First Build to Final Robot

This section summarizes the **practical build timeline**. Adjust the text to match what you actually did.

1. **Low-fidelity prototype (paper/cardboard):**
   - Quickly tested the four-bar geometry.
   - Verified that pushing down on the coupler produced a forward “hop”.
2. **Refined laminated prototype:**
   - Switched to laminated layers for more consistent link stiffness.
   - Added flexure hinges and proper servo mounting.
3. **Final build:**
   - Cleaned up the DXFs and link dimensions.
   - Tuned rubber bands / flexure thickness to match the optimized stiffness from simulation.
   - Recorded videos for **Experimental Validation**.

Throughout the process, I iterated between:

- **Simulation** (updating link lengths and hinge stiffness in MuJoCo), and  
- **Physical builds** (measuring actual performance and adjusting the design).

---

## 7. Practical Tips & Lessons Learned

- **Tolerances:**  
  Holes cut exactly to nominal diameter may be too tight. Slightly oversize servo/bolt holes in the DXF to make assembly easier.
- **Hinge durability:**  
  Flexure joints made only from paper can fatigue quickly. Combining paper with a thin plastic layer extends life.
- **Lamination quality:**  
  Uneven glue or bubbles can warp the links. Apply adhesive uniformly and press under weight.
- **Sim-to-real mismatch:**  
  Friction, backlash, and material non-idealities mean the real robot will never match the simulation perfectly.
  Use the **Experimental Validation** page to explicitly document these differences.

---

## 8. Link to Other Sections

- [System Model (MuJoCo)](system-model.html) – defines the geometry and stiffness that this manufacturing plan implements.
- [Design Optimization](optimization.html) – explains how the chosen dimensions and hinge stiffness were optimized.
- [Experimental Validation](experimental-validation.html) – shows how the manufactured robot performs compared to the model.
- [Report & Video](report-and-video.html) – final summary and video demonstration of the robot in action.

[Watch the final presentation video](https://YOUR-VIDEO-LINK-HERE)
