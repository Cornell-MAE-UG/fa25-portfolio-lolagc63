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

Compute beam angle at the top position (tip = 0.50 m):

{% raw %}
<script type="math/tex; mode=display">
	heta = \arcsin\left(\frac{y_{\mathrm{tip}}}{L}\right) = \arcsin\left(\frac{0.50}{1.20}\right) = 0.4297754313\ \mathrm{rad} = 24.624^{\circ}
</script>
{% endraw %}

Coordinates:

- Tip \(T\): {% raw %}<script type="math/tex">(L\cos\theta,\;L\sin\theta) = (1.2\cos\theta,\;1.2\sin\theta) \approx (1.09087121\ \mathrm{m},\;0.50000000\ \mathrm{m})</script>{% endraw %}
- Actuator-to-beam pin (attachment) \(P\) with \(a = 1.00\ \mathrm{m}\):
	- {% raw %}<script type="math/tex">P=(a\cos\theta,\;a\sin\theta)\approx(0.90905934\ \mathrm{m},\;0.41666667\ \mathrm{m})</script>{% endraw %}

Actuator ground point used: {% raw %}<script type="math/tex">G_2=(1.00,\;0)\ \mathrm{m}</script>{% endraw %}

![Free body diagram]({{ '/assets/images/fbd_lin_act.jpeg' | relative_url }}){: .block-image}

## Summary

Add any additional notes, calculations, or results here. You can copy portions from the original project and adapt them as needed.
