---
layout: project
title: Extra Credit - ENGRD 2020
description: Analyzing a device
technologies: []
image: 
---

## Thermodynamic Analysis of Heating Demand for Duffield Hall

This report analyzes a real system that we interact with daily: **Duffield Hall**, an academic and laboratory building on Cornell University’s campus in Ithaca, NY. The goal is to apply thermodynamic principles from class—specifically control volumes, mass balance, energy balance, and entropy considerations—to estimate the heating energy required to maintain a constant indoor temperature under winter conditions, and to examine how changes in operating conditions affect performance.

---

## Description of the System

Duffield Hall is a large, multi-story engineering building that contains laboratories, classrooms, and office spaces. During winter operation, the building must be heated continuously to offset heat losses to the cold outdoor environment. Heat is supplied by Cornell’s campus heating system, while heat is lost through the building envelope (walls, windows, roof) and through infiltration of outdoor air.

For this analysis, the building is treated as a **control volume** operating at steady state over a representative time period.

---

## Control Volume and Interactions

The control volume is drawn around the entire building.

- **Heat input:** thermal energy supplied by the heating system, $ \dot{Q}_{in} $
- **Heat output:** heat lost to the environment through walls, windows, roof, and infiltration, $ \dot{Q}_{loss} $
- **Mass flow:** infiltration of outdoor air and exfiltration of indoor air (assumed equal at steady state)

No shaft work is produced by the building itself, so work interactions are neglected at this level of analysis.

---

## Governing Equations

### Mass Balance

At steady state, the mass flow rate of air entering the building due to infiltration is approximately equal to the mass flow rate leaving:

$$
\dot{m}_{in} \approx \dot{m}_{out}
$$

This assumption allows the total mass of air inside the building to remain constant over time.

---

### Energy Balance (First Law)

For steady operation with constant indoor temperature, the energy balance reduces to:

$$
\dot{Q}_{in} = \dot{Q}_{loss}
$$

The building heat loss is modeled using a lumped heat-transfer relation:

$$
\dot{Q}_{loss} = U A (T_{in} - T_{out})
$$

where  
- $U$ is the overall heat transfer coefficient of the building envelope  
- $A$ is the effective exterior surface area  
- $T_{in}$ is the indoor temperature  
- $T_{out}$ is the outdoor temperature  

---

### Entropy Balance (Second Law)

Heat transfer from the warm indoor space to the colder outdoor environment occurs across a finite temperature difference and is therefore irreversible. As a result, entropy is generated during operation:

$$
\dot{S}_{gen} > 0
$$

Entropy generation arises from conductive heat transfer through the envelope and mixing of indoor and outdoor air due to infiltration. This explains why continuous energy input is required to maintain indoor comfort.

---

## Assumptions and Data

To perform a first-pass analysis, the following assumptions are used:

- Indoor temperature setpoint: $T_{in} = 20^\circ \text{C}$
- Outdoor winter design temperature: $T_{out} = -10^\circ \text{C}$
- Effective building envelope area: $A \approx 10{,}000 \ \text{m}^2$
- Average overall heat transfer coefficient: $U \approx 0.5 \ \text{W/m}^2\cdot\text{K}$

These values are representative of a large, modern academic building with significant glazing.

---

## Heating Load Calculation

The temperature difference between indoors and outdoors is:

$$
\Delta T = T_{in} - T_{out} = 20 - (-10) = 30 \ \text{K}
$$

The heating power required to offset heat loss is:

$$
\dot{Q}_{loss} = (0.5)(10{,}000)(30) = 150{,}000 \ \text{W}
$$

or

$$
\dot{Q}_{loss} = 150 \ \text{kW}
$$

Thus, Duffield Hall requires approximately **150 kW of continuous heating power** to maintain indoor temperature when it is −10°C outside.

The daily heating energy required is:

$$
E_{day} = 150 \times 24 = 3{,}600 \ \text{kWh/day}
$$

---

## Effect of a Change in Operating Conditions

To examine the effect of colder outdoor temperatures, consider:

- New outdoor temperature: $T_{out} = -20^\circ \text{C}$

The new temperature difference is:

$$
\Delta T = 20 - (-20) = 40 \ \text{K}
$$

The new heating requirement becomes:

$$
\dot{Q}_{loss,new} = (0.5)(10{,}000)(40) = 200{,}000 \ \text{W}
$$

or

$$
\dot{Q}_{loss,new} = 200 \ \text{kW}
$$

This represents a **33% increase in required heating power** compared to the baseline case.

---

## Discussion and Interpretation

This analysis shows that heating demand scales linearly with the indoor–outdoor temperature difference under steady-state conditions. Even moderate decreases in outdoor temperature significantly increase the required heating power. This explains why campus heating systems must be designed for worst-case winter conditions.

The model also highlights the importance of building envelope performance. A reduction in the overall heat transfer coefficient $U$—through improved insulation, better windows, or reduced infiltration—would directly reduce heating demand at all outdoor temperatures.

---

## Conclusion

Duffield Hall can be modeled as a steady-state thermodynamic control volume during winter operation. Using reasonable assumptions and basic thermodynamic principles, the heating energy required to maintain indoor comfort was estimated and shown to increase significantly as outdoor temperature decreases. This study demonstrates how concepts from thermodynamics can be applied directly to real campus infrastructure and building energy performance.
