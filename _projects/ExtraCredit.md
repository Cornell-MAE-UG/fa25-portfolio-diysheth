---
layout: project
title: Extra Credit - ENGRD 2020
description: Analyzing a device
technologies: []
image: 
---

# Thermodynamic Analysis of Heating Demand for Duffield Hall (Cornell University)

For this extra credit assignment, I analyze a real-world system that we interact with daily: **Duffield Hall**, an academic and laboratory building on Cornell University’s campus in Ithaca, NY. The goal is to apply the thermodynamic principles from class—specifically control volumes and energy balances—to estimate how much energy is required to heat the building under different outdoor temperature conditions, and to analyze how changes in operating conditions affect system performance.

---

## Description of the Device/System

Duffield Hall is a large, multi-story engineering building that houses classrooms, offices, and laboratories. During the winter, the building must be heated continuously to maintain a comfortable indoor temperature despite cold outdoor conditions. Heat is supplied to the building through Cornell’s campus heating system (steam-based), while heat is lost to the surrounding environment through the building envelope and air infiltration.

From a thermodynamics perspective, Duffield Hall can be treated as a **control volume** operating at steady state over a given time period. The indoor air temperature is assumed constant, meaning that the rate of heat input from the heating system must balance the rate of heat loss to the outdoors.

---

## Control Volume and Interactions

The control volume is drawn around the entire building.

- **Heat input:** thermal energy supplied by the heating system, \( \dot{Q}_{in} \)
- **Heat output:** heat lost to the environment through walls, windows, roof, and infiltration, \( \dot{Q}_{loss} \)
- **Mass flow:** infiltration of outdoor air and exfiltration of indoor air (assumed equal at steady state)

No shaft work is produced by the building itself, so work interactions are neglected at this level of analysis.

---

## Governing Equations

### Mass Balance

At steady state, the mass flow rate of air entering the building due to infiltration is approximately equal to the mass flow rate leaving:

\[
\dot{m}_{in} \approx \dot{m}_{out}
\]

This assumption allows the building air mass to remain constant over time.

---

### Energy Balance (First Law)

For steady operation with constant indoor temperature:

\[
\dot{Q}_{in} = \dot{Q}_{loss}
\]

The heat loss from the building is modeled using a standard lumped heat-transfer relation:

\[
\dot{Q}_{loss} = U A (T_{in} - T_{out})
\]

where:
- \( U \) is the overall heat transfer coefficient of the building envelope,
- \( A \) is the effective exterior surface area,
- \( T_{in} \) is the indoor air temperature,
- \( T_{out} \) is the outdoor air temperature.

---

### Entropy Balance (Second Law)

Heat transfer from the warmer indoor space to the colder outdoor environment occurs across a finite temperature difference and is therefore irreversible. As a result, entropy is generated during building operation:

\[
\dot{S}_{gen} > 0
\]

Sources of entropy generation include conductive heat transfer through the envelope and mixing of indoor and outdoor air due to infiltration. This irreversibility explains why continuous energy input is required to maintain indoor comfort.

---

## Assumptions and Data

To perform a first-pass analysis, the following assumptions are made:

- Indoor setpoint temperature:  
  \( T_{in} = 20^\circ \text{C} \)
- Outdoor winter design temperature (baseline case):  
  \( T_{out} = -10^\circ \text{C} \)
- Effective building envelope area:  
  \( A \approx 10{,}000 \, \text{m}^2 \)
- Average overall heat transfer coefficient:  
  \( U \approx 0.5 \, \text{W/m}^2\cdot\text{K} \)

These values are representative of a large, modern academic building with a significant amount of glazing.

---

## Baseline Heating Load Calculation

The temperature difference between indoors and outdoors is:

\[
\Delta T = T_{in} - T_{out} = 20 - (-10) = 30 \, \text{K}
\]

The heating power required to offset heat loss is then:

\[
\dot{Q}_{loss} = (0.5)(10{,}000)(30) = 150{,}000 \, \text{W}
\]

\[
\dot{Q}_{loss} = 150 \, \text{kW}
\]

This means Duffield Hall requires approximately **150 kW of continuous heating power** to maintain indoor temperature when it is −10°C outside.

Over a full day, the energy required is:

\[
E_{day} = 150 \times 24 = 3{,}600 \, \text{kWh/day}
\]

---

## Effect of a Change in Operating Conditions

To examine how system performance changes, consider a colder outdoor temperature:

- New outdoor temperature:  
  \( T_{out} = -20^\circ \text{C} \)

The new temperature difference is:

\[
\Delta T = 20 - (-20) = 40 \, \text{K}
\]

The new heating requirement becomes:

\[
\dot{Q}_{loss,new} = (0.5)(10{,}000)(40) = 200{,}000 \, \text{W}
\]

\[
\dot{Q}_{loss,new} = 200 \, \text{kW}
\]

This represents a **33% increase in required heating power** compared to the baseline case. This result shows that heating demand scales linearly with outdoor temperature difference for this steady-state model.

---

## Discussion

This analysis demonstrates how a simple thermodynamic energy balance can be used to estimate real building energy demands. Even moderate drops in outdoor temperature can significantly increase heating requirements, which explains why campus heating systems must be sized for worst-case winter conditions. The model also highlights the importance of building envelope design: reducing the overall heat transfer coefficient \( U \) through better insulation or improved windows would directly reduce heating energy consumption at all outdoor temperatures.

---

## Conclusion

Duffield Hall can be effectively modeled as a steady-state thermodynamic control volume during winter operation. Using reasonable assumptions and standard heat-transfer relations, the heating demand was estimated for typical Ithaca winter conditions and shown to increase substantially as outdoor temperature decreases. This study connects thermodynamic theory from class directly to a real, campus-scale engineering system and illustrates how operating conditions influence energy performance.





