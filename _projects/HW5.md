---
layout: project
title: Piston Problem - ENGRD 2020
description: mechanical design problem
technologies: [Autodesk Fusion]
image: assets/images/IMG_0023.jpg
---


# Problem Definition
The goal is to design a 2D linkage that fits inside a **150 cm × 50 cm** window and can lift the **maximum load** to the **maximum height** using one fixed-length bar, three pin supports (two on the ground), and a linear actuator. All parts are rigid, and the analysis is static.

# Constraints & Objectives
- Mechanism must stay inside **1500 mm × 500 mm**
- Ground pins **A** and **B** are **300 mm** apart
- Chosen bar lengths:
  - Main bar: **450 mm**
  - Strut: **200 mm**
- Actuator force limited to catalog **max force**
- **Objective:** maximize lifting force and vertical travel

# Degrees of Freedom
The mechanism has 4 links (ground, main bar, strut, actuator) and 5 pin joints.  
Gruebler’s equation gives:

$$
DOF = 3(4-1) - 2(5) = -1 
$$

The variable-length actuator adds one DOF → system behaves as a **1-DOF mechanism**.

# Static Analysis Summary
For each actuator length, link geometry is solved to find the bar angles.  
Taking moments about the ground pin gives:

$$
W \cdot d_{\text{load}} = F_a \cdot d_{\text{act}} 
$$

Thus,

$$
W = F_a \left(\frac{d_{\text{act}}}{d_{\text{load}}}\right) 
$$

This shows the mechanism lifts the most weight when the actuator has a large moment arm and the load moment arm is small. The chosen link lengths and support locations were selected to maximize this mechanical advantage while staying inside the design window.
