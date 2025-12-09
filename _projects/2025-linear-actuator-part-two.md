---
layout: project
title: Linear Actuator — Part Two
description: Follow-up analysis for the linear actuator mechanism
technologies: [Google Sheets]
image: /assets/images/linear_act.png
---

## Overview / assumptions
**Geometry (selected configuration)**

- Bar length: L = 1.20 m
- Tip height: y_tip = 0.50 m

**Modeling assumptions**

- Beam modeled as an Euler–Bernoulli beam (small-deflection, linear theory).
- Boundary condition: cantilever (fixed) at the pivot. The pivot hub is assumed stiff enough to provide rotational restraint (conservative assumption for deflection).

**Loads included (transverse components only)**

- Tip vertical load: W = 31,630 N (value from actuator equilibrium calculation).
- Actuator peak thrust: F_a = 35,810 N. For bending we include only the component of this thrust perpendicular to the beam at the actuator attachment point P.

**Material & properties**

- Steel: E = 200 GPa, ρ = 7850 kg/m³.

**Serviceability limit**

- Allowable tip vertical deflection: 2% of L (0.02 L).


## Preliminary geometry / kinematics

- Compute beam angle at top position: θ = arcsin(y_tip/L) = arcsin(0.50/1.20) = 0.4297754213 rad = 24.624 degrees
- Coordinates:
    - Tip T = (Lcosθ, Lsinθ)
    - Actuator-to-beam(attatchment)P = (acosθ, asinθ) with a = 1.00m
    - with a = 1.00: P≈(0.90905934 m,0.41666667 m)
- Actuator ground point used: G2 = (1.00, 0)m

## Compute actuator transverse component at P (vector method)







## compute actuator component at P (vector method)

You can view the full calculation (PDF) here:

[Download my Calculations]({{ "/assets/Compute Actuator Transverse Component at P (Vector method) ~ Calculations_.pdf.pdf" | relative_url }}) in PDF format.

![Free body diagram]({{ '/assets/images/fbd_lin_act.jpeg' | relative_url }}){: .block-image}

## Summary

Add any additional notes, calculations, or results here. You can copy portions from the original project and adapt them as needed.
