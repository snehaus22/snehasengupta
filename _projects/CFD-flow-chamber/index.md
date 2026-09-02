---
layout: post
title: Computational Fluid Dynamic Modeling of Variable-Height Flow Chamber for Cell Stress Analysis
description:  A computational model to study how changing channel geometry affects shear stress on adherent cells. Using COMSOL Multiphysics, I built 2D and 3D CFD models of a variable-height flow chamber designed for cell stress experiments. I simulated fluid velocity and shear stress profiles along the chamber length and compared numerical results to analytical shear stress equations. I analyzed how geometric constraints influenced local stress gradients and validated model behavior under laminar flow assumptions.
skills: 
- COMSOL
- Computational Fluid Dynamics
- Newtonian Fluids
- Cell/Tissue Engineering
- Tissue Biomechanics
main-image: /cfdflowchamber.png
---

## Introduction
Computational fluid dynamics (CFD) modeling is a powerful cost-efficient simulation tool meant for characterizing and analyzing fluid behavior within a specified geometry. For the fluid flow chamber, the decreasing height of the chamber increases the velocity of the fluid as it moves further along the chamber, increasing the stress applied to the cells on the bottom plate. The ability to iteratively manipulate the model within the constraints of the pharmaceutical product makes CFD an essential, cost-effective tool for optimizing both design and performance.

## Methods
In the pre-processing stage, the parallel plate flow chamber was constructed in COMSOL. The width, length, and outlet height was fixed, so a changed angle varied only the height of the inlet. The structure was first designed in 2D and then later extruded into the complete 3D model. Boundary conditions and initial conditions were inputted into COMSOL to specify fluid properties relevant to this study such as viscosity and density. In solving, COMSOL iteratively solved for velocity, pressure, and shear stress distributions across the chamber using the Finite-Element Method (FEM).

When it comes to fluid properties and physics manipulations, standard equations were applied for calculating the Reynolds number and the volumetric flow rate. The initial conditions limited the Reynolds number to 125 which in combination with the shear stress and shear rate data, allowed for calculations of the velocity for the outlet of the chamber. This, along with the knowledge of the area of the outlet allowed for calculation of the volumetric flow rate which is maintained in each flow chamber, no matter what inlet height is used. This volumetric flow rate and other constants, along with the calculated viscosity, provided the values necessary to calculate the shear stress along the bottom plate where the endothelial cells are located. The shear stress that was calculated using Equation 1 formed the analytical solution.
{% include image-gallery.html images="shearstresseq.png" height="400" %} 

## Results
In order to fall within the < 1% error without causing extreme shear stress on the cells on the bottom plate of the chamber, the final angle of the top surface of the chamber was 0.4 degrees.

Image of the velocity vectors illustrating the velocity profile at the chamber exit in COMSOL where the gradient bar on the right side is the velocity.
{% include image-gallery.html images="velocity.png" height="400" %} 

A contour plot of the shear stress along the bottom of the flow chamber.
{% include image-gallery.html images="shearstress.png" height="400" %} 

