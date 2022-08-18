---
layout: post
title:  "More on wetting in very large systems with cross-shaped geometry"
date:   2022-08-18 09:52:03 +0100
categories: [active wetting]
typora-root-url: ../../docs
---

### VERY large systems with cross-shaped geometry

I pushed the simulations a bit further and simulated very large 3D systems with $L_x = L_y = 120\sigma$ and a thinner transverse dimension $L_z = 20\sigma$, at density $\rho=0.75$ so that I simulate N = 216000 particles for 300$\tau_r$.  



![image-20220817120426500](/images/WeetingCrossGeom/eps8-lx603D.png)

*Density at $\varepsilon=8$ in a system with size $L_x=120\sigma$*.





The following animations illustrate the relaxation to the steady state at different barrier strengths

|                    $\varepsilon=8$                     |                     $\varepsilon=10$                     |                     $\varepsilon=20$                     |                     $\varepsilon=30$                     |
| :----------------------------------------------------: | :------------------------------------------------------: | :------------------------------------------------------: | :------------------------------------------------------: |
| ![mov-eps8.0](/images/WeetingCrossGeom/mov-eps8.0.gif) | ![mov-eps10.0](/images/WeetingCrossGeom/mov-eps10.0.gif) | ![mov-eps20.0](/images/WeetingCrossGeom/mov-eps20.0.gif) | ![mov-eps30.0](/images/WeetingCrossGeom/mov-eps30.0.gif) |

There is some asymmetry in the profiles at low $\varepsilon$ but - as we have previously discussed - it is made probably rather complex by cross interactions across quadrants.

On these scales, I think that it appears more evident that the low-density region changes from having a convex interface (high $\varepsilon$) to a concave one (low $\varepsilon$).
