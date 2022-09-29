---
layout: post
title:  "Active wetting in corner geometry"
date:   2022-09-21 21:30:03 +0100
categories: [active wetting]
typora-root-url: ../../docs
---



# Corner geometry

 

Running large simulations with $L_x=100\sigma$ for 700 $\tau_r$

| $\varepsilon$ |                 time average of the density                  |
| :-----------: | :----------------------------------------------------------: |
|      10       | ![eps10.0-hist-data-dl1.0.h5.avg](/images/WettingCornerGeom/avgs/eps10.0-hist-data-dl1.0.h5.avg.png) |
|      12       | ![eps12.0-hist-data-dl1.0.h5.avg](/images/WettingCornerGeom/avgs/eps12.0-hist-data-dl1.0.h5.avg.png) |
|      14       | ![eps14.0-hist-data-dl1.0.h5.avg](/images/WettingCornerGeom/avgs/eps14.0-hist-data-dl1.0.h5.avg.png) |
|      16       | ![eps16.0-hist-data-dl1.0.h5.avg](/images/WettingCornerGeom/avgs/eps16.0-hist-data-dl1.0.h5.avg.png) |
|      18       | ![eps18.0-hist-data-dl1.0.h5.avg](/images/WettingCornerGeom/avgs/eps18.0-hist-data-dl1.0.h5.avg.png) |
|      20       | ![eps20.0-hist-data-dl1.0.h5.avg](/images/WettingCornerGeom/avgs/eps20.0-hist-data-dl1.0.h5.avg.png) |
|      30       | ![eps30.0-hist-data-dl1.0.h5.avg](/images/WettingCornerGeom/avgs/eps30.0-hist-data-dl1.0.h5.avg.png) |



Note: there are significant finite size effects in the time required to nucleate the high density phase at small $\varepsilon$. For example. For example, for $\varepsilon=10$, I can observe the formation of MIPS and the "wetting" above but not for $L_x=40\sigma$, even after 1500 $\tau_r$, indicating that we are entering a regime dominated by homogeneous nucleation. 

In fact, keeping $L_x=50\sigma$, we can decrease $\varepsilon$ further and see again that the time to observe MIPS becomes much longer. So, I can follow another route: I prepare a system at $\varepsilon=10$ and reduce the strength of the barrier instantaneously. What I observe is that the density is readjusted very rapidly, and the density per quadrant becomes stationary very quickly, e.g.

![stationarity](/images/WettingCornerGeom/avgs/eps4-time.png)



The pictures above would indicate that reducing the strength disfavours wetting and that around $\varepsilon=10$ we are in an almost neutral condition (the apparent contact angle is around 90 degrees). Can we get larger angles? Instantaneous snapshots of the system are intriguing, as in the following case at $\varepsilon=4$



![image-20220929164452025](/images/WettingCornerGeom/instantaneaous-eps4-continue.png)

They would suggest thatthe droplet deforms and still its boundary would be modified by the presence of the wall, promoting contact in a region close to the corner and not away from it. 

However, if we take a time-averaged picture we see the following

| $\varepsilon$ | Density                                                      |
| ------------- | ------------------------------------------------------------ |
| 10            | <img src="/images/WettingCornerGeom/avgs/eps10.0-hist-data-dl1.0.h5.avg.png" alt="eps10.0-hist-data-dl1.0.h5.avg" style="zoom:80%;" /> |
| 8             | <img src="/images/WettingCornerGeom/avgs/eps8-continue.png" alt="eps8-continue" style="zoom:80%;" /> |
| 6             | <img src="/images/WettingCornerGeom/avgs/eps6-continue.png" alt="eps6-continue" style="zoom:80%;" /> |
| 4             | <img src="/images/WettingCornerGeom/avgs/eps4-continue.png" alt="eps4-continue" style="zoom:80%;" /> |

Seen from this point of view, it appears that the high-density region simply gradually distances itself from the barrier, and for $\varepsilon=6$ the average density profile already has a circular shape.



Further insight can be gleaned by looking at the density fluctuations. If we measure, for example,  the variance of the density profiles, we observe an interesting trend:![variances](/images/WettingCornerGeom/avgs/variances.png)



It would appear that $\varepsilon=10$ corresponds to a regime where fluctuations are maximal in amplitude and spatial extent, and that these dampen below and above this value. How to understand this.

Clearly, they are very much suppressed in the high $\varepsilon$, where wetting is strong, meaning that the density profile is well-localised. As the strength is decreased, the interface away from the wedge changes curvature and presents a significant increase in its fluctuations. Note, in fact, that it is only as we decrease $\varepsilon$ that this interface should become more and more similar to a free interface of MIPS in its fluctuations.

The fact that for $10<\varepsilon<20$ the fluctuations appear to penetrate inside the droplet could be interpreted as a consequence of global rearrangements of large parts of the droplet itself. The scale associated with these rearrangements appears to peak for $\varepsilon=10$. Below this value (where notably the protocol is different nad the data come from a quench), the fluctuations appear again confined to the free surface. This again makes sense, as in the limit of $\varepsilon=0$ we would expect the variance to be maximal at the interface and very low both inside and outside of the droplet.
