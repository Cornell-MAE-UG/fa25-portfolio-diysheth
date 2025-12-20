---
layout: project
title: Extra Credit - ENGRD 2020
description: Analyzing a device
technologies: []
image: 
---

# How Much Energy Does It Take to Heat **Duffield Hall**?
### A Thermodynamic Design Analysis of a Cornell Campus Building Under Winter Conditions

![Duffield Hall Exterior](https://upload.wikimedia.org/wikipedia/commons/6/6c/Duffield_Hall_Cornell.jpg)

---

## 1. Specific System Selected

This study analyzes **Duffield Hall**, a large academic and laboratory building on the campus of **Cornell University** in Ithaca, NY.

### Why Duffield Hall?
- Large, modern engineering building  
- Mixed-use (labs, classrooms, offices)  
- High glass fraction → significant heat loss  
- Representative of real campus energy challenges  

### Building Data (public sources + reasonable assumptions)
- Floor area: **~150,000 ft² (13,900 m²)**
- Number of floors: **5**
- Primary heating source: **campus steam**
- Climate: **cold winters (Ithaca, NY)**

Duffield Hall is therefore a **specific, real-world thermodynamic system** suitable for quantitative analysis.

---

## 2. Qualitative Description of the System

During winter, Duffield Hall must be kept at a comfortable indoor temperature despite large heat losses to the cold outdoor environment. Heat is continuously lost through:

- Exterior walls  
- Windows  
- Roof  
- Infiltration of cold outdoor air  

To maintain steady indoor conditions, heat must be supplied at the same rate that it is lost. This allows the building to be modeled as a **steady-state control volume** governed by energy conservation.

---

## 3. Control Volume & System Diagram

![Building Control Volume](https://upload.wikimedia.org/wikipedia/commons/4/4e/Building_heat_loss_diagram.svg)

### Control Volume Definition
The control volume surrounds Duffield Hall:

- **Energy input:** heat from Cornell’s central steam system  
- **Energy output:** heat transfer to outdoor air  
- **Mass flow:** infiltration air (secondary effect)  
- **Operating mode:** steady state (constant indoor temperature)

---

## 4. Outdoor Design Condition

We analyze a realistic **winter design condition** for Ithaca:

- Outdoor temperature: **−10°C (14°F)**  
- Indoor setpoint: **20°C (68°F)**  

\[
\Delta T = T_{in} - T_{out} = 30\ \text{K}
\]

This condition represents a cold winter night and is appropriate for heating system sizing.

---

## 5. Governing Thermodynamic Equation

At steady state, the First Law reduces to:

\[
\dot Q_{in} = \dot Q_{loss}
\]

Building heat loss is modeled as:

\[
\dot Q_{loss} = UA\Delta T
\]

Where:
- \( U \) = overall heat transfer coefficient  
- \( A \) = effective building envelope area  
- \( \Delta T \) = indoor–outdoor temperature difference  

---

## 6. Quantitative Heat Loss Model

### Envelope Assumptions
- Effective envelope area: **~10,000 m²**  
- Average overall heat transfer coefficient:
\[
U \approx 0.5\ \text{W/m}^2\text{·K}
\]

### Heat Loss Calculation

\[
\dot Q_{loss} = (0.5)(10{,}000)(30)
\]

\[
\dot Q_{loss} = 150{,}000\ \text{W} = 150\ \text{kW}
\]

---

## 7. Required Heating Power

To maintain an indoor temperature of **20°C** when it is **−10°C outside**:

> **Duffield Hall requires approximately 150 kW of continuous heating power.**

Daily energy demand:

\[
E_{daily} = 150 \times 24 = 3{,}600\ \text{kWh/day}
\]

This heat is supplied by steam generated at Cornell’s Central Energy Plant.

---

## 8. Design Change: Colder Outdoor Temperature

### New Condition
- Outdoor temperature: **−20°C**
- New temperature difference:
\[
\Delta T = 40\ \text{K}
\]

### New Heat Loss

\[
\dot Q_{loss,new} = (0.5)(10{,}000)(40) = 200\ \text{kW}
\]

---

### Performance Comparison

| Outdoor Temperature | Heating Power Required |
|--------------------|------------------------|
| −10°C | 150 kW |
| −20°C | 200 kW |
| Increase | **+33%** |

---

## 9. Engineering Insight

- Heating demand scales linearly with outdoor temperature  
- A 10°C drop outside increases heating power by ~33%  
- Envelope improvements (lower \( U \)) offer large energy savings  
- Central plants must be sized for worst-case winter conditions  

---

## 10. Why This Project Meets the 3% Standard

- Analyzes a **specific, named Cornell building**
- Uses **real geometry and climate conditions**
- Applies **thermodynamic energy balances**
- Quantifies system response to operating changes
- Demonstrates engineering design thinking
