---
layout: project
title: Linear Actuator Design
description: ENGRD 2020 Assignment 5, Fall 2025
technologies: [Google Sheets]
image: /assets/images/linear_act.png
---

# Single-Link Lifting Mechanism — Portfolio Entry

> **Project goal:** design a 2D lifting mechanism (inside a 150 cm × 50 cm envelope) that reaches the highest tip height (50.0 cm), and for that height maximize static lift using the actuator's peak thrust.

---

## Objective
The assignment mixes two goals:

> “…lift the maximum possible weight to the highest possible height.”

I interpret this as the following objectives:

- **Primary:** Reach the maximum allowable tip height within the 50.0 cm vertical envelope.  
- **Secondary:** For that configuration, maximize the static weight that can be lifted/held using the actuator’s **peak** thrust.

This entry documents a simple single-link design that hits 50.0 cm tip height and computes the maximum static weight for that configuration.

---

## Mechanism choice (2D single-bar linkage)

- **Pivot (Pin 1):** \(G_1=(0,0)\) (ground).  
- **Actuator ground pin (Pin 2):** \(G_2=(0.90,0)\).  
- **Actuator-to-bar pin (Pin 3):** point \(P\) at distance \(a\) from the pivot along the bar.  
- **Bar (boom):** rigid length \(L\).  
- **Load:** vertical point load \(W\) at the bar tip.

---

## Design parameters (initial case)

| Parameter | Symbol | Value |
|---|---:|:---|
| Envelope | — | 150 cm × 50 cm |
| Bar length | \(L\) | 1.00 m |
| Tip height target | \(y_tip\) | 0.50 m |
| Actuator peak thrust | \(F_a\) | 35.81 kN = 35,810 N (IMA55 RNO5) |
| Max actuator stroke | — | 457 mm |
| Actuator base | \(G_2\) | (0.90 m, 0) |
| Actuator attach point | \(a\) | 0.85 m |

---
