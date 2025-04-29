---
title: "Fluid Simulation with FLIP"
excerpt: "<br/><iframe width='560' height='315' src='https://www.youtube.com/embed/wCsaSCDQsKA' </iframe>"
collection: portfolio
---

Built a fluid simulation referencing methods from [Fluid Simulation Using Implicit Particles](https://www.danenglesson.com/images/portfolio/FLIP/rapport.pdf) and [Fluid Flow for the Rest of Us: Tutorial of the Marker and Cell Method in Computer Graphics](https://cg.informatik.uni-freiburg.de/intern/seminar/gridFluids_fluid_flow_for_the_rest_of_us.pdf).

The simulation combines the Fluid-Implicit Particles (FLIP) and Particle-In-Cell (PIC) methods to achieve an optimal mix of low and high frequency effects (i.e. viscous and turbulent flow). The fluid-implicit particle method updates particle velocities by adding the interpolated change of the velocity field. The particle-in-cell method updates particle velocities by setting them to the interpolated value of the velocity field.

First the initial fluid and solid positions are initialized with input triangle meshes. We initialize a dynamic MAC (Marker and Cell) grid
For each timestep loop
* A timestep is computed based on the CFL condition
* Particle velocities are transferred to the field
* Boundary conditions are enforced on the field
* Divergence is removed from the field via a pressure-solve, thereby conserving mass
* Particle velocities are then derived from the field (using interpolated FLIP+PIC)
* And finally, particles are advected (i.e. moved) through the field.
At every time step the particle positions are saved. Triangle meshes are then reconstructed from the point cloud data by converting it to a Signed Distance Field and applying the Marching Cubes algorithm. We used Blender to render each frame.
