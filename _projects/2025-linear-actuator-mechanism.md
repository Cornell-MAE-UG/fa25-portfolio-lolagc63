---
layout: project
title: Linear Actuator Design
description: ENGRD 2020 Assignment 5, Fall 2025
technologies: [Google Sheets]
image: /assets/images/linear_act.png
---

 **Project goal:** 
 Design a 2D lifting mechanism (inside a 150 cm × 50 cm envelope) that reaches the highest tip height (50.0 cm), and for that height maximize static lift using the actuator's peak thrust.

 ---

## Objective
The assignment mixes two goals:

> “…lift the maximum possible weight to the highest possible height.”

I interpret this as the following objectives:

- **Primary:** Reach the maximum allowable tip height within the 50.0 cm vertical envelope.  
- **Secondary:** For that configuration, maximize the static weight that can be lifted/held using the actuator’s **peak** thrust.

---

## Mechanism choice (2D single-bar linkage)

- **Pivot (Pin 1):** \(G_1=(0,0)\) (ground).  
- **Actuator ground pin (Pin 2):** \(G_2=(0.90,0)\).  
- **Actuator-to-bar pin (Pin 3):** point \(P\) at distance \(a\) from the pivot along the bar.  
- **Bar:** rigid length \(L\).  
- **Load:** vertical point load \(W\) at the bar tip.

---

## Free-Body Diagram

![Free body diagram]({{ '/assets/images/fbd_lin_act.jpeg' | relative_url }}){: .block-image}

---

## Design Parameters (initial case)

- Envelope: 150 cm x 150 cm (given)
- Bar Length (L): 1.00 m
- Tip Height Target (y_tip): 0.50 m
- Actuator: IMA55 RN05
- Actuator Peak Thrust (F_a): 35.81 kN
- Actuator Max Stroke: 457 mm
- Actuator Base (G_2): (0.90 m, 0.00 m)
- Actuator Attatch Point (a): 0.85 m

Note: The bar length was chosen to be 1.00 m because it keeps the tip of the bar inside 150 cm horizontally and allows it to reach a 50 cm vertical at a reasonable angle (calculated in next part). It is also important to note that the attatch point (a) is 0.85 m because it is within the max stroke (also calculated in next section).

---

## Geometry at top position (tip = 0.50 m)

- **Bar Angle**: We know that Lsinθ is 0.50 m therefore θ = 30 degrees
- **Coordinates**: We know that T = (Lcosθ, Lsinθ) = (0.8660m, 0.500m)
- **Actuator-bar attachment P**: We know that P = (acosθ, asinθ) = (0.737m, 0.425m)
- **Actuator length**: 0.456m = 4556mm - this is within the 457mm stroke limit

---

## Maximum Weight Calculation

**Idea**: At static equilibrium the actuator must provide a moment about the pivot that balances the moment due to the vertical weight at the tip.

[Download my Calculations]({{ "/assets/max_weight.pdf" | relative_url }}) in PDF format.

**W = 34,762 N = 3,544 kg**

---