---
layout: project
title: Extra Credit - ENGRD 2020
description: Analyzing a device
technologies: []
image: 
---

# Heating Load Analysis of Duffield Hall (Cornell University)

This report applies thermodynamic principles to a real system: **Duffield Hall**, a campus building at Cornell University. The objective is to estimate the heating power required to maintain a constant indoor temperature under winter conditions and to evaluate how outdoor temperature affects performance.

---

## System Description

![Duffield Hall]([https://upload.wikimedia.org/wikipedia/commons/6/6c/Duffield_Hall_Cornell.jpg](https://www.vermontstructuralslate.com/wp-content/uploads/2018/04/DSC_0018-1-1354x900.jpg))

Duffield Hall is a multi-story academic and laboratory building heated by Cornell’s campus steam system. During winter, heat is lost to the environment through the building envelope and air infiltration. The building is modeled as a steady-state control volume.

---

## Control Volume and Interactions

The control volume includes the entire building.

- Heat input from the heating system: $ \dot{Q}_{in} $
- Heat loss to the environment: $ \dot{Q}_{loss} $
- Mass flow due to air infiltration and exfiltration (assumed equal at steady state)

No shaft work is produced by the building.

---

## Governing Equations

### Mass Balance

At steady state:

$$
\dot{m}_{in} \approx \dot{m}_{out}
$$

---

### Energy Balance (First Law)

For constant indoor temperature:

$$
\dot{Q}_{in} = \dot{Q}_{loss}
$$

Heat loss is modeled as:

$$
\dot{Q}_{loss} = U A (T_{in} - T_{out})
$$

---

### Entropy Consideration

Heat transfer across a finite temperature difference is irreversible, so:

$$
\dot{S}_{gen} > 0
$$

---

## Assumptions

- Indoor temperature: $T_{in} = 20^\circ \text{C}$
- Outdoor winter temperature: $T_{out} = -10^\circ \text{C}$
- Envelope area: $A \approx 10{,}000 \ \text{m}^2$
- Overall heat transfer coefficient: $U \approx 0.5 \ \text{W/m}^2\cdot\text{K}$

---

## Heating Load Calculation

Temperature difference:

$$
\Delta T = 30 \ \text{K}
$$

Heating power required:

$$
\dot{Q}_{loss} = (0.5)(10{,}000)(30) = 150 \ \text{kW}
$$

Daily energy use:

$$
E_{day} = 3{,}600 \ \text{kWh/day}
$$

---

## Effect of Outdoor Temperature

For $T_{out} = -20^\circ \text{C}$:

$$
\Delta T = 40 \ \text{K}
$$

$$
\dot{Q}_{loss,new} = 200 \ \text{kW}
$$

This is a **33% increase** in heating power compared to the baseline case.

---

## Conclusion

Duffield Hall can be modeled as a steady-state thermodynamic control volume. Heating demand increases linearly with outdoor temperature difference, demonstrating how environmental conditions directly affect building energy performance.
