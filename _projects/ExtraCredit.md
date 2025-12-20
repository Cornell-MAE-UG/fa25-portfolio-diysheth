
layout: project
title: Extra Credit - ENGRD 2020
description: Analyzing a device
technologies: []
image: 


# Heating Load Analysis of Duffield Hall (Cornell University)

 **Duffield Hall**, is an Engineering building at Cornell University.In this portfolio I am trying to estimate the heating power that is required to maintain a constant indoor temperature under the harsh winter conditions. I am also trying to evaluate how outdoor temperature affects performance.



## System Description

<p align="center">
  <img src="https://www.vermontstructuralslate.com/wp-content/uploads/2018/04/DSC_0018-1-1354x900.jpg"
       alt="Duffield Hall"
       width="400">
</p>

Duffield Hall is a an academic and laboratory building heated by Cornell’s campus steam system. During winter, heat is lost to the environment through the building envelope and air infiltration. The building is modeled as a steady-state control volume system.


## Control Volume and Interactions

The control volume includes the entire building.

- Heat input from the heating system: $ \dot{Q}_{in} $
- Heat loss to the environment: $ \dot{Q}_{loss} $
- Mass flow due to air infiltration and exfiltration (assumed equal at steady state)

No shaft work is produced by the building, so work interactions are neglected.

---

## Governing Equations

### Mass Balance

At steady state, the mass flow rate of air entering the building is approximately equal to the mass flow rate leaving:

$$
\dot{m}_{in} \approx \dot{m}_{out}
$$

---

### Energy Balance (First Law)

For steady operation with constant indoor temperature:

$$
\dot{Q}_{in} = \dot{Q}_{loss}
$$

Rather than modeling detailed heat transfer through individual building components, the building heat loss is assumed to be **proportional to the indoor–outdoor temperature difference**:

$$
\dot{Q}_{loss} = C (T_{in} - T_{out})
$$

where $C$ is a constant that depends on the building’s construction and heat-loss characteristics.

---

### Entropy Consideration

Heat transfer from the warm indoor space to the colder outdoor environment occurs across a finite temperature difference and is therefore irreversible. As a result, entropy is generated:

$$
\dot{S}_{gen} > 0
$$

---

## Assumptions

- Indoor temperature: $T_{in} = 20^\circ \text{C}$
- Outdoor winter temperature (baseline case): $T_{out} = -10^\circ \text{C}$
- Operation is steady state
- Heating power required at baseline conditions is approximately 150 kW

---

## Determination of the Building Constant

For the baseline condition:

$$
T_{in} - T_{out} = 20 - (-10) = 30 \ \text{K}
$$

Given a heating requirement of 150 kW:

$$
150 = C (30)
$$

Solving for the building constant:

$$
C = 5 \ \text{kW/K}
$$

---

## Heating Load Calculation

Using the proportional model:

$$
\dot{Q}_{loss} = 5 (T_{in} - T_{out})
$$

At the baseline condition:

$$
\dot{Q}_{loss} = 5 (30) = 150 \ \text{kW}
$$

The corresponding daily energy use is:

$$
E_{day} = 150 \times 24 = 3{,}600 \ \text{kWh/day}
$$

---

## Effect of Outdoor Temperature

For a colder outdoor temperature of $T_{out} = -20^\circ \text{C}$:

$$
T_{in} - T_{out} = 20 - (-20) = 40 \ \text{K}
$$

The new heating requirement is:

$$
\dot{Q}_{loss,new} = 5 (40) = 200 \ \text{kW}
$$

This represents a **33% increase** in required heating power compared to the baseline case.

---

## Conclusion

Duffield Hall was modeled as a steady-state thermodynamic control volume using a simple proportional heat-loss model. The analysis shows that the heating power required to maintain indoor comfort increases linearly with the indoor–outdoor temperature difference. This demonstrates how outdoor environmental conditions directly influence building energy demand and highlights the usefulness of basic thermodynamic principles for analyzing real engineering systems.
