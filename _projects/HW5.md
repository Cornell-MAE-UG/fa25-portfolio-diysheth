---
layout: project
title: Piston Problem - ENGRD 2020
description: mechanical design problem
technologies: [Autodesk Fusion]
image: assets/images/IMG_0023.jpg
---

# Problem

Given a 2D design space of **150 cm long** and **50 cm tall**, a rigid bar of a fixed length (your choice), **3 pin supports** (two mounted on the ground), and a **linear actuator** chosen from the provided catalog (max force only), the task is to design a mechanism that can **lift the maximum possible weight** to the **maximum possible height**.  
All bars, supports, and the actuator are assumed rigid for this first part of the analysis.

The mechanism I designed is shown in the sketch above.

---

# Constraints / Objectives

### **Geometric Constraints**
- Entire mechanism must fit inside a **150 cm × 50 cm** rectangular design window.
- Two pin supports must be placed on the ground plane (in my design, points **A** and **B**, 300 mm apart).
- Bar lengths in my design:  
  - Main lifting bar: **450 mm**  
  - Secondary strut: **200 mm**  
  - Actuator link: **150 mm**

### **Actuator Constraints**
- Must use a model from the provided actuator catalog (max force rating only).
- Must not cause interference during motion.
- Must generate enough moment about ground support **A** to lift the load.

### **Design Objectives**
1. **Lift the greatest possible weight** the actuator can statically support.  
2. **Achieve the largest possible vertical lift height** for the end point of the main bar.

---

# Design Degrees of Freedom

This is a **1-DOF pin-jointed mechanism** driven by a linear actuator.

- Points **A** and **B** are fixed ground supports.
- Joint **C** connects the actuator to the main lifting bar.
- The actuator extension determines the rotation of the 450 mm bar about point **A**.
- The location of joints A, B, C, and bar lengths determine the full motion path of the lifted point **K**.

---

# Static Analysis (Rigid-Bar Approximation)

To determine the load the mechanism can lift, I treated all bars as rigid and analyzed the **moment balance about point A**.

The actuator applies a force $F_{\text{act}}$ at joint **C**, creating a moment:

$$
M_{\text{act}} = F_{\text{act}} \, r_{AC} \sin(\theta_{AC})
$$

The load at point **K** produces an opposing moment:

$$
M_{\text{load}} = W \, r_{AK} \sin(\theta_{AK})
$$

Static equilibrium requires:

$$
F_{\text{act}} \, r_{AC} \sin(\theta_{AC})
=
W \, r_{AK} \sin(\theta_{AK})
$$

Where:

- $r_{AC} = 200\ \text{mm}$  
- $r_{AK} = 450\ \text{mm}$  
- $\theta_{AC}$ and $\theta_{AK}$ depend on the actuator and bar orientation.

Solving for the liftable weight:

$$
W = F_{\text{act}}
\left( \frac{r_{AC}}{r_{AK}} \right)
\left( \frac{\sin(\theta_{AC})}{\sin(\theta_{AK})} \right)
$$

This expression shows that the lift capacity depends heavily on the geometry and the angles.  
The mechanism lifts the most weight when the bar is steep (large $\sin\theta$) and the least when horizontal.

In my design, actuator contraction raises point **C**, rotating the 450 mm main bar upward and lifting point **K** through the dashed arc (≈ 200 mm height), while staying within the 50 cm height limit.

---

# Final Mechanism (Rigid-Bar Model)

The final design includes:

- Ground supports at **A** and **B** (300 mm apart)  
- Main lifting bar: **450 mm**  
- Secondary bar: **200 mm**  
- Actuator bar: **150 mm**  
- Joint **C** as actuator attachment point  
- Load carried at point **K** near the tip of the 450 mm bar  

The actuator retracts to raise the bar and extend to lower it, creating a simple, controllable 1-DOF lifting mechanism.
