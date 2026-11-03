# ExoticCompactObjectRingdown

This is a collection of Mathematica notebooks and files that aim to numerically solve the equations for the quasi-normal modes (QNMs) of a background metric. They constitue the main work for my master thesis within the Master Degree in Astrophysics and Space Physics of Università Milano Bicocca.

## Aims

The first goal is to develop a direct integration method that finds the QNMs of a known background metric. Specifically, the equations governing the perturbations of the target metric are required. My work focuses on Schwarzschild metric for non-rotating black holes (BHs) and exotic compact objects (ECOs), and on Kerr metric for rotating BHs and ECOs with arbitrary spin.

The second goal is to compute the QNMs spectrum (or, at least, part of it) of spinning ECOs. The latter are described through the membrane paradigm which allows to map the specific physics of an ECO to a fictitious fluid located at the ECO surface. Doing so, just two parameters, the viscosity and the shear of the fluid, are able to define univocally the entire space of exotic objects.

## Methods

A direct integration method is adopted. The differential equation governing the perturbation is integrated from two limits: the event horizon (surface in the case of ECOs) and infinity. The results are glued together at a match point of choice. The QNM is estimated by smoothing the solution at the match point.

Two sets of boundary conditions (BCs) are needed, one at the horizon (surface), the other at infinity. While the latter depends solely on the metric, the former is determined by the specific nature of the object, hence using the membrane paradigm. When achievable, an approximate solution is computed through a series expansion and then used as BC. This procedure improves the final result.

See `QNM_Schwarzschild.nb`, `QNM_Kerr.nb` and `QNM_HorizonlessCO.nb` for the implementation in the specific instances.

## Analysis

The results for Schwarzschild and Kerr BHs can be compared to the analytical solutions. Relative to ECOs, previous results obtained with different methods (among which the continued fractions method) are used as reference.

In `QNM_compute.nb` routines computing QNMs with different sets of varing parameters and hyperparameters are implemented.
