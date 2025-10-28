---
layout: post
title: "Multi-Layered Golf Ball (FEA Analysis)"
date: 2025-01-10
last_modified_at:
image:
  path: /docs/images/200golf2.png
  thumbnail: /docs/images/golfball.png
  caption: "SolidWorks render of a golfball"
---
A custom golf ball modeled with a core, mantle, and outer shell, using composite materials. Performed finite element analysis to evaluate energy absorption and deformation across each layer. This study explored how materials and wall thicknesses affect performance. My report can be seen below:

The goal of this study was to analyze how a three-layer golf ball responds to a static compressive load of 200 N using SolidWorks Simulation. The model was built with three distinct layers: a polybutadiene core, a polyurethane mantle, and an outer shell made of cross-linked polyethylene (XLPE). These materials were chosen to mirror the elasticity, strength, and durability found in real golf balls. The geometry was carefully defined, with a core radius of 36 mm, a mantle radius of 38.5 mm, and an outer shell radius of 42.67 mm. Each layer was bonded to the next to allow smooth stress transfer and prevent delamination under load.

The polybutadiene core was assigned an elastic modulus of 2 N/mm², a density of 930 kg/m³, and a Poisson’s ratio of 0.49, giving it a soft, energy-absorbing character. The polyurethane mantle, with an elastic modulus of 35 N/mm², a density of 1,200 kg/m³, and a Poisson’s ratio of 0.47, served as an intermediate layer to aid energy transfer. The XLPE outer shell was stiffer, with an elastic modulus of 200 N/mm², a density of 940 kg/m³, and a Poisson’s ratio of 0.46, providing the surface rigidity and impact resistance necessary for performance. To simulate realistic conditions, the bottom of the golf ball was fixed to represent ground contact, and a 200 N vertical load was applied to the top surface.

Several setup challenges had to be resolved before achieving a stable simulation. Initially, missing elastic modulus values in the material library caused solver errors, which were fixed by creating fully defined custom materials. Another issue that popped up was the error message “model not stable”, which occurred due to missing fixtures and was corrected by applying a fixed constraint to the base. Early runs also failed because of missing bonded interactions between layers, which I resolved by switching to global bonded contacts and later to node-to-surface bonding, which greatly improved model stability and convergence. The mesh was kept relatively coarse to maintain reasonable solve times after finer meshes caused excessive computation delays.

Once stabilized, the simulation ran successfully and produced consistent results. The maximum von Mises stress reached about 1.3 × 10^7 N/m² near the point of load application, while the maximum displacement was approximately 0.9 mm and the maximum equivalent strain was around 0.05 (5%). The stress distribution showed realistic deformation patterns, high stresses concentrated near the impact area, gradually dissipating through the mantle and core. The outer shell held its shape effectively, while the inner layers absorbed and distributed the force, confirming that the layered design balances energy absorption with surface durability.

The study highlights not only the mechanical performance of the modeled golf ball but also the importance of careful setup in simulation work, accurate material definitions, correct boundary conditions, and stable contact configurations are essential for producing meaningful and reliable engineering insights.


