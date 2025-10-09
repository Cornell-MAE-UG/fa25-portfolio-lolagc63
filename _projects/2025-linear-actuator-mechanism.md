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

## Additional Case (L = 1.20 m)

To explore geometric effects, I evaluated a second configuration keeping the 150 cm × 50 cm envelope and 457 mm stroke limit. 

- L = 1.20 m
- θ = 24 degrees
- G_2 = (1.00, 0.00)
- a = 1.00 m
- Actuator Length = 420 mm
- d_perpendicular = 0.968 m
- **W = 31, 626 N**
- **M = 3,224 kg**

---

## Trends

| Case | L (m) | G₂ (m) | a (m) | Stroke (mm) | d⊥ (m) | W (N) | m (kg) | Feasible? |
|---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | 1.00 | 0.90 | 0.85 | 456 | 0.84 | 34,760 | 3,544 | yes |
| 2 | **1.20** | **1.00** | **1.00** | **420** | **0.97** | **31,630** | **3,224** | yes |
| 3 | 1.20 | 0.80 | 1.00 | 398 | 0.88 | 28,600 | 2,917 | yes |
| 4 | 1.20 | 1.20 | 1.00 | 458 | 1.01 | 32,800 | 3,345 | no |
| 5 | 1.20 | 1.00 | 0.80 | 374 | 0.81 | 26,300 | 2,682 | yes |
| 6 | 1.20 | 1.00 | 1.20 | 465 | 1.04 | 33,800 | 3,446 | no |

---

## Conclusions
- Both \(L=1.00\) m and \(L=1.20\) m designs can meet stroke and envelope limits; the 1.20 m bar increases reach while slightly reducing capacity.  
- Increasing \(G_2\) increases leverage and \(W\), but risks exceeding stroke.  
- Decreasing \(a\) increases mechanical advantage but reduces vertical range.  
- **Balanced recommendation:** L=1.20m, G_2=(1.00,0), a=1.00 

---

### Notes / practical considerations
- Numbers above use **peak thrust**. For sustained designs use continuous thrust (~12.23 kN)
- A brake or lock is required to prevent back-drive in vertical applications (Tolomatic note).  

---