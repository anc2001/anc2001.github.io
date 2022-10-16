---
title: "Tree Generation with SP-GAN"
date: 2022-01-13
description: "Trained SP-GAN on a dataset of procedurally generated Trees"
summary: "Trained SP-GAN on a dataset of procedurally generated trees to generate even more trees :evergreen_tree:"

showReadingTime : false
showWordCount : false
showEdit: false
---

## Overview
<a target="_blank" href="https://github.com/anc2001/SP-GAN"> {{< icon "Github" >}}Github Link</a>

A dataset of procedurally generated trees was created with the blender addon [Treegen](https://github.com/friggog/tree-gen). These trees were then converted into point clouds with Poisson disk sampling. The model [SP-GAN](https://github.com/liruihui/SP-GAN) was trained for 300 epochs on this point cloud data. 

## Results
Latent Space Interpolation
![](featured.png)

SP-GAN morphs a sphere of points into the final pointcloud. Correspondence between points on the starting sphere and the final pointcloud is shown below. 

![](correspondence.png)
