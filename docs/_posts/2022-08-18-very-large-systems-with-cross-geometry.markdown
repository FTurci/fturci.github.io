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

*Density field at $\varepsilon=8$ in a system with size $L_x=120\sigma$*.





The following animations illustrate the relaxation to the steady state at different barrier strengths

|                    $\varepsilon=8$                     |                     $\varepsilon=10$                     |                     $\varepsilon=20$                     |                     $\varepsilon=30$                     |
| :----------------------------------------------------: | :------------------------------------------------------: | :------------------------------------------------------: | :------------------------------------------------------: |
| ![mov-eps8.0](/images/WeetingCrossGeom/mov-eps8.0.gif) | ![mov-eps10.0](/images/WeetingCrossGeom/mov-eps10.0.gif) | ![mov-eps20.0](/images/WeetingCrossGeom/mov-eps20.0.gif) | ![mov-eps30.0](/images/WeetingCrossGeom/mov-eps30.0.gif) |

There is some asymmetry in the profiles at low $\varepsilon$ but - as we have previously discussed - it is made probably rather complex by cross interactions across quadrants.

On these scales, I think that it appears more evident that the low-density region changes from having a convex interface (high $\varepsilon$) to a concave one (low $\varepsilon$). therefore, I have tried to quantify the **curvature** of these interfaces.



## Curvatures

I use a level set to identify the curvature. I coarse grain the density (as in the videos above) and choose a level set at the diameter density $\rho_{diam}=0.85$. This defines segmented curves in 2D through which I can fit a spline curve to extract the curvature at every point. I can then associate a curvature value to every contour either by taking the **average** of the curvatures or the **median**. Since, in fact, the curves present some pointed regions at small epsilons, some outliers need to be removed to compute the mean.



| $\varepsilon=10$                                         | $\varepsilon=40$                                         |
| -------------------------------------------------------- | -------------------------------------------------------- |
| ![frame296](/images/WeetingCrossGeom/contours/eps10.jpg) | ![frame209](/images/WeetingCrossGeom/contours/eps40.png) |

The probability distribution function of the curvature at steady state is non-Gaussian.

![boxplot](/images/WeetingCrossGeom/contours/pdfs.png)

The curvature captures aspects of the transition (again, the order is not clear):

![medians](/images/WeetingCrossGeom/contours/stats.png)
