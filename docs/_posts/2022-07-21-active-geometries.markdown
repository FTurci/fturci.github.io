---
layout: post
title:  "Geometries in active wetting"
date:   2022-07-21 09:52:03 +0100
categories: [active wetting]
typora-root-url: ../../docs
---

Tuneable repulsive barriers acting on phase-separated active Brownian particles lead to transitions analogous to complete to partial wetting in equilibrium.

The original geometry of the [2021 PRL]([10.1103/PhysRevLett.127.238002](https://doi.org/10.1103/PhysRevLett.127.238002)) consisted of a single barrier in an elongated box that promoted phase separation.

Here we explore different geometries, with the aim to stabilise droplet-like structures (if possible).



## Geometry 1: the cross

The simplest modification we consider is to couple two barriers in the x and y direction of the simulation box. For convenience, $\varepsilon$ identifies the barrier strength. The simulations are run for a total of $200\tau_r$ rotational diffusion times, which is enough to attain a steady state in most conditions (but we may want to run even longer simulations to check the possibility of slow relaxation of the interfaces).



### In two dimensions

In two dimensions, I observe the gradual transformation from a completely wet cross to the formation of accumulation in the corners of the cross, with large fluctuations from time frame to time frame and from quadrant to quadrant.

![2dcross](/images/WeetingCrossGeom/2dcross-eps24-32-48.png)

The fluctuations for weak barrier strengths are very strong, but it is maybe still possible to define time windows over which the density profiles in a quadrant are quasi-stationary



![2deps24](/images/WeetingCrossGeom/2d-eps24.gif)

### In three dimensions 

In this exploratory work - to save computation time - I have taken a system of unequal sizes $L_x = L_y= 2L_z = 40$. The dimension $z$ corresponds to the depth in the following plots and is therefore thinner than the other dimensions.  This also make averages across z more significative as the geometry still promotes the slab instead of a sphere MIPS aggregate, as illustrated here below (the colour coding represents the local density within a cutoff radius at the second minimum of g(r), $3.1\sigma$).

![3dcross-eps12-24](/images/WeetingCrossGeom/thickness-eps8.png)



We can look at lateral profiles to map the qualitative changes as the repulsive strength varies.



![3dcross-eps12-24](/images/WeetingCrossGeom/3dcross-eps12-24.png)



As $\varepsilon$ decreases, the profiles become more asymmetric and the density accumulates around the cross.

Even smaller $\varepsilon$ lead to the formation of a (strongly fluctuating) droplet that gets localised around the cross. For example, for $\varepsilon=8$ we have:

![epsilon8animation](/images/WeetingCrossGeom/eps8.gif)



We can also identify a meaningful density contour. By choosing a suitable threshold (here $\rho=0.80$ ), we can separate the high and low-density regions and identify the (2d) projection of their lateral density profile

![3dcross-eps12-14-contour](/images/WeetingCrossGeom/contours3d.png)



the contours **fluctuate**. They can - for example - cross the barrier.

![crossing](/images/WeetingCrossGeom/eps12-crossing-avg080.npy.png)

##### Contour length

A simple quantity to describe the contours is the total length $\ell_{contour}$ which is the sum of all contours of each contour length. The quantity fluctuates significantly over the simulation, so here the bars represent **standard deviations** over the trajectory. Note that the (sharp) transition in 3d is around $\varepsilon\approx18-20$. Here we observe a gradual increase in the contour length that peaks around $\varepsilon=12$ and decreases below this value. 



![lcontour](/images/WeetingCrossGeom/lcontour.png)

The decrease is due to a qualitative change: below $\varepsilon=12$  we mostly identify a single contour that never spans the system size. This suggests that some fine-tuning of the contour threshold may be required.
