---
title: "Finite Element Method"
date: 2022-03-22
description: "a"
summary: "Finite Element Physics Collision Simulation"

showReadingTime : false
showWordCount : false
showEdit: false
---
## Demo Video
{{< youtube HX46C2uimWY >}}

Shown in order
- Single tetrahedron falling on the floor.
- Cube falling on the floor.
- Sphere falling on a fixed sphere.
- Ellipsoid falling on a fixed sphere with a tilted plane

## Description
Project is a finite element simulation for general triangle meshes. The strain, stress, and resulting force exerted at every element is computed at every timestep and used to integrate the simulation forward. Collisions between elements and a static plane are also supported. 

