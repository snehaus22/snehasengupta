---
layout: post
title: Toxicokinetics of BPA on the Human Body
description:  A mathematical model of BPA absorption and endocrine disruption in the human body. My team developed a compartmental model simulating BPA absorption, distribution, metabolism, and excretion, incorporating endocrine system interactions. We also modeled pharmacokinetics of therapeutic agents and immune cell dynamics in parallel projects, using differential equations to capture system behavior over time.
skills: 
- Python
- Chemical Kinetics
- Pharmacokinetics/Pharmacodynamics
- Differential Equations
main-image: /bpa.png
---

## Intro
To explore the safety of BPA, we constructed a physiologically accurate toxicokinetic (TK) model of BPA to evaluate its effects on human health. By contrasting a healthy system with one subjected to BPA exposure exceeding FDA guidelines, differences in estrogen, testosterone, and insulin levels were explored along with the impact on fertility and diabetes risk. After I designed mass balance equations and compartmental models tracking the flow of BPA and these hormones within the reproductive system, we tested differing frequencies and intensities of BPA dosages to examine the impact.

## Methods
The estrogen equation above calculates the concentration of BPA in the uterus based on the assumptions that only 1% of BPA that is ingested makes its way to the uterus via the bloodstream and that only free BPA (including unconjugated) can impact the estrogen receptors in the uterus. The second term in this equation reduces the overall value of (production rate of granulosa cells) by 20%-50% once the threshold of BPA that actually damages the estrogen receptor pathways is reached as expected. 

Estrogen Equations and Parameters
{% include image-gallery.html images="estrogentable.png" height="400" %} 

{% include image-gallery.html images="estrogengraph.png" height="400" %} 
Number of Granulosa Cells in the Uterus over time after Constant 200 µg/kg BW per day Intake

## Results
The figure above shows a 2% reduction in granulosa cell production when ingesting 200 ug/kg-day, far above this threshold. An exponential decrease in granulosa cell production was expected, especially within the first 24 hours, with the largest drop observed during this period. Once the granulosa cell production rate plateaued, the reduction in production shows a marginal decrease overall.

The results show that after a single sudden intake of 100 µg BPA/kg body weight, the body effectively excretes nearly all of it over the course of a day. Contrary to common belief, the intake of BPA is not as rare as some think since BPA is present in common foods and everyday items. Consequently, this means that BPA actually does not pose a serious threat to the average individual, even after a substantial intake of BPA.
