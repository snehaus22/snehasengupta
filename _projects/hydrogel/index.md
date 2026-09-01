---
layout: post
title: Low-Cost Microneedle Hydrogel Continuous Glucose Monitor
description:  We proposed a low-cost, electronic-free, microneedle (MN) hydrogel patch CGM that utilizes colorimetric glucose detection to continuously monitor glucose levels. The proposed MN hydrogel includes glucose oxidase (GOx) to convert glucose into gluconic acid and bromocresol purple (BCP) to allow for colorimetric detection of pH changes resulting from gluconic acid levels. To detect a patient’s glycemic status, the MN hydrogel penetrates the skin and absorbs interstitial fluid containing glucose. This glucose then reacts with glucose oxidase, producing gluconic acid and decreasing the pH of the hydrogel. As glucose levels increase, decreasing pH levels are reported by a color change from purple to yellow facilitated by BCP. I created and executed the equations for transport phenomena to create a digital twin of our hydrogel model in COMSOL Multiphysics.
skills: 
- COMSOL Multiphysics
- Biochemistry
- 3D Modeling
- Hydrogel Fabrication
main-image: /hydrogelga.png
---

## Hydrogel Manufacturing Workflow
{% include image-gallery.html images="hydrogelmold.png" height="400" %} 
This system was validated through a combination of in vitro experiments and COMSOL computational modeling to assess performance at physiologically relevant glucose concentrations. The resulting hydrogels demonstrated reversible and dynamic color changes in response to changing glucose levels, supporting their potential for continuous monitoring applications. A quantitative image-based analysis method further enabled estimates of glucose concentration with high accuracy. Microneedle arrays were successfully fabricated, although optimization of mechanical strength and diffusion kinetics remain necessary.


## COMSOL Digital Twin
To compare glucose transport and enzymatic reaction kinetics between the hydrogels with and without MNs, a three-dimensional computational model was developed in COMSOL Multiphysics. The GOx-catalyzed oxidation of glucose to gluconolactone and hydrogen peroxide was modeled sequentially and followed by spontaneous hydrolysis of gluconolactone to gluconic acid.

{% include image-gallery.html images="hydrogelcomsol.png" height="400" %} 

A simplified flat interface geometry was created to model the non-MN condition. Glucose diffused progressively into the bulk hydrogel, establishing a concentration gradient with highest concentrations near the entry interface. Enzymatic reaction rates were greatest near this surface, producing gluconolactone that accumulated and diffused inward. Hydrolysis to gluconic acid reactions created a heterogenous pH distribution with the greatest acid presence near the glucose entry point.
### Glucose diffusion gradient across hydrogel base and microneedles using Fick's 2nd Law
{% include image-gallery.html images="hydrogelcomsol.png" height="400" %} 

Subsequently, a digital twin of the MN hydrogel was created. Modeling diffusion of glucose from the MN tips into the base revealed that 2.7 hours were necessary for complete saturation of the hydrogel, compared to 2.5 hours for the non-MN hydrogel. This corroborates the results of the previous experiment.

Although the non-MN hydrogel simulation resulted in faster complete glucose saturation than the MN hydrogel simulation, these models failed to account for the heterogeneous distribution of glucose in the skin. MN hydrogels must penetrate 250-1000 μm (Saifullah and Rad 2023) into the skin in order to access and absorb ISF, thus validating the MN design. Moreover, the concentration gradient appeared more homogenous in the MN hydrogel than in the flat interface

