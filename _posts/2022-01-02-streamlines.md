---
layout: post
title: Fluid Simulation from Scratch
subtitle: The SIMPLE Way
---

> I'm Hydrodynamically Designed!

-[Spongebob Squarepants](https://youtu.be/USEnoc6B9zw)

## Why?

Over the last semester, (*the fall of 2021 for you historians*), I took a class called "Computational Fluid Mechanics and Heat Transfer". Our professor, Dr. Hanif Montazeri, promised a challenging/rewarding experience; frankly, he undersold it. Over the course of 4 months, we hand-crafted our own solvers for the famous [Navier-Stokes Equations](https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations). I learned a lot about vector-calculus, discretizing equations, and good programming practice, but most importantly, I made some pretty graphs.

## Solvers Specifics

The solver I wrote for this class was written in Python and made extensive use of the SciPy sparse linear algebra library. I used the SIMPLE (Semi-Implicit Method for Pressure Linked Equations) algorithm on a co-located grid. This algorithm was first proposed by [Patankar and Spalding](https://doi-org.myaccess.library.utoronto.ca/10.1016/0017-9310(72)90054-3) in 1973 [1] and its implementation on a co-located grid was first described by [Rhie and Chow](https://doi.org/10.2514/3.8284) in 1983 [2]. I promise the pretty graphs are coming.


## The Principle Problem

The scope of the course was to simulate the famous "Lid-Driven Cavity" flow problem. This is a well-known benchmark for testing fluid simulations and has been studied numerically and experimentally for decades. The idea is to simulate how a fluid would behave in a square box with an open top where fluid was rushing past:

![Lid Driven Cavity](..\assets\img\streamlines\liddrivencavity.png){: .mx-auto.d-block :}
<figcaption align = "center"><i>Geometry of lid-driven cavity flow problem by OpenFOAM</i></figcaption>

[Ghia et al.](https://doi-org.myaccess.library.utoronto.ca/10.1016/0021-9991(82)90058-4) [3] wrote a landmark paper in 1982 studying the problem on a high resolution grid. I used their results to verify the correctness of my own solver, which are the first pretty plots I present below:

![Compared](..\assets\img\streamlines\compare.png){: .mx-auto.d-block :}
<figcaption align = "center"><i>Comparison streamlines: my solver (left) and Ghia et al. (right) for lid-driven cavity flow</i></figcaption>

My solver seemed to be accurate enough and I was happy that it captured the small eddies forming in the corners. I also conducted a more involved grid independence study and I compared the velocity profiles through the geometric center of the cavity. These graphs are much less interesting, so for now I hope my readers can take my word for it.

## More Interesting Problems

The real beauty of having a solver is that you can go beyond the state-mandated solutions. While developing my code, I made sure to make it 

## References

[1] S. V. Patankar and D. B. Spalding, “A calculation procedure for heat, mass and momentum transfer in three-dimensional parabolic flows,” International Journal of Heat and Mass Transfer, vol. 15, no. 10, pp. 1787–1806, Oct. 1972, doi: 10.1016/0017-9310(72)90054-3.

[2] C. M. Rhie and W. L. Chow, “Numerical study of the turbulent flow past an airfoil with trailing edge separation,” AIAA Journal, vol. 21, no. 11, pp. 1525–1532, Nov. 1983, doi: 10.2514/3.8284.

[3] U. Ghia, K. N. Ghia, and C. T. Shin, “High-Re solutions for incompressible flow using the Navier-Stokes equations and a multigrid method,” Journal of Computational Physics, vol. 48, no. 3, pp. 387–411, Dec. 1982, doi: 10.1016/0021-9991(82)90058-4.
