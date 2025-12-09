---
layout: project
title: Piston Problem - ENGRD 2020
description: mechanical design problem
technologies: []
image: assets/images/IMG_0023.jpg
---

## Problem Definition
Given a 2D design space of 150cm long and 50cm tall, a bar of a fixed length (your choice), 3 pin supports of which two need to be mounted on the ground and a linear actuator (pick from this online catalog, use max force values only), design a frame/mechanism to lift the maximum possible weight to the highest possible height. Assume all the support and actuator are rigid

## Constraints & Objectives
- Mechanism must stay inside 1500 mm × 500 mm
- Ground pins A and B are 300 mm apart
- Chosen bar lengths:
  - Main bar: 450 mm
  - Distance from A to C: 200 mm
- Actuator force limited to catalog **max force**
- Objective: maximize lifting force and vertical travel

## Degrees of Freedom
The mechanism has 1 DOF from the actuator stroke.

## Static Analysis Summary (Rigid Bar)

To choose the final geometry, I treated the lifting bar as completely rigid and evaluated how the actuator force would rotate it about the ground pivot. I compared the bar’s position at the start and end of the motion to see where the actuator produced the strongest torque and whether the bar stayed within the 1500 × 500 mm space.

By checking how effectively the actuator pushed on the bar at different angles, I confirmed that placing the attachment point 200 mm from the pivot and spacing the ground pins 300 mm apart gave good leverage throughout the lift. The bar could move smoothly from about 30° to 75° without hitting the boundries, while still producing enough lifting capability using the Tolomatic IMA55 actuator. This analysis guided the final placement of the pins and ensured the mechanism could achieve a practical lift height with realistic actuator stroke and loading.

# Step 2: Flexible Bar (Beam) Analysis

## (a) Maximum deflection and assumptions  
For this step I treated the 450 mm lifting bar as a beam instead of rigid.  
Assumptions:
- Pin A is the fixed support
- The payload hangs at the tip of the bar.
- Only the components of these forces perpendicular to the bar create bending.
- The bar has a uniform 20 × 30 mm hollow rectangular cross-section in aluminum 6061-T6.

I estimated the worst case tip deflection in the middle position. The total vertical deflection at the tip comes out to only a few millimeters, comfortably below the 9 mm (2% of 450 mm) limit.

## (b) Beam design for < 2% deflection  
To keep deflection under 2% while minimizing mass, I chose an aluminum tube since it has a good stiffness to weight ratio.

Final beam choice:
- Material: Aluminum 6061-T6  
- Cross-section: 20 mm × 30 mm rectangular tube  
- Wall thickness: 2 mm  
- Length: 450 mm  

This section is stiff enough that the calculated deflection stays well under 9 mm for the design loads.

## (c) Final beam design

![IMG_8345](https://github.com/user-attachments/assets/ab38aaba-0657-4c71-9f82-7c456ebd3c55)
