---
layout: project
title: Linear Actuator — Part Two
description: Follow-up analysis for the linear actuator mechanism
technologies: [Google Sheets]
image: /assets/images/linear_act.png
---

**Project goal:** 
 Choose a beam design (cross-section, material) such that its vertical deflection is below 2% of its length and is the most mass-efficient possible.


 ---

## Overview / assumptions
1. Geometry used: selected configuration L = 1.20m, tip height y_tip = 0.50m
2. Beam modeled as an Euler-Bernoulli beam
3. Boundary condition: fixed at pivot (assumed stiff enough to provide rotational restraint)
4. Loads included (transverse components only):
    - Tip vertical load W = 31, 630 N 
    - Actuator Peak Thrust (F_a): 35,810 N; only its component perpendicular to the beam at the actuator point P is used for bending
5. Material: steel, E = 200GPa, ρ = 7850 kg/m^3
6. Allowable tip vertical deflection = 2% of L = 0.02L

 ---

## Preliminary geometry / kinematics
1. Beam angle at top position:
    θ = arcsin(y_tip/L​​) = arcsin(0.50/1.20​) = 0.4297754313 rad = 24.624∘
2. Coordinates:
    - Tip T = (Lcosθ,Lsinθ)
    - Actuator-to-beam pin (attachment) P = (acosθ,asinθ) with a = 1.00 m
    - P ≈ (0.90905934 m,0.41666667 m)
3. Actuator ground point used: G_2 = (1.00,0)m

 ---

## Calculating actuator transverse component at P

You can view the detailed calculation (PDF) here:

<a href="{{ '/assets/Compute Actuator Transverse Component at P (Vector method) ~ Calculations_.pdf' | relative_url }}" target="_blank" rel="noopener noreferrer">Compute Actuator Transverse Component at P (Vector method) — Calculations (PDF)</a>

 ---

## Maximum deflection in the beam
Model: beam (fixed at x = 0), with
- tip vertical point load W at x = L,
- transverse point load F⊥ at x = a

You can view the detailed calculation (PDF) here:

<a href="{{ '/assets/Maximum Deflection Calculations.pdf' | relative_url }}" target="_blank" rel="noopener noreferrer">Compute Actuator Transverse Component at P (Vector method) — Calculations (PDF)</a>

---

## Choosing a beam cross-section
Design Stretegy:
- For bending stiffness per unit mass, thin-walled large-diameter hollow sections are efficient (large I for small area).
- Choose a realistic manufacturable wall thickness (avoid <1 mm unless composite). I used t = 2.0 mm (practical steel tube) and selected the minimum outer diameter D that satisfies I ≥ I_req and fits envelope constraints. 

Selected Section:
- Hollow circular steel tube
    - Outer diameter D = 0.209 m = 209 mm
    - Wall thickness t = 0.002 m = 2.0 mm

Section properties Calculations:

---






 




