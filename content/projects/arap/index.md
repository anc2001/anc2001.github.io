---
title: "ARAP"
date: 2022-04-08
description: "ARAP"
summary: "Implementation of the paper As-Rigid-As-Possible Surface Modeling"

showReadingTime : false
showWordCount : false
showEdit: false
---
## Demo Video
{{< youtube rCRaXV7d-Ik >}}

Shown are simple examples constraining mutliple different vertices and seeing that the mesh deform reasonably. 

## Description
Program builds matrix `L` based on equation 8 in the paper, applies constraints by deleting corresponding rows and columns of constrained vertices, and then constructs and solves a linear system of equations described in the paper with `Eigen::SimplicialLDLT`. 

