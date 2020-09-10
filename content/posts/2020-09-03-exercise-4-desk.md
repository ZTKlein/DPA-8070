---
template: post
title: "Exercise 4:  Desk"
slug: ex-4-desk
draft: false
date: 2020-09-09T03:45:47.707Z
description: Our fourth exercise was to model a desk
category: Exercises
tags:
  - exercises
---
## Problem:

Model a desk. I decided to make everything using only one starting primitive.

## Solution:

I started off with a basic block for a desk, and added a few edge loops to allow extruding in the center. I then tried using multicut to get appropriate topology for the drawers.

![Multicut](/media/ex4_drawers_multicut.PNG "Multicut drawers")

I quickly found out, however, that doing it like this led to topology issues, so I started from scratch and made sure to use edge loops for EVERYTHING. The only times I used multicut was to clean up topology that I broke (which happened far more often than I'd like to admit). In the end, I'm happy with what I managed to achieve using only edge loops, scaling, and extruding.

![Nonsmooth](/media/ex4_nonsmooth.PNG "Final result")
![Wireframe](/media/ex4_wireframe.PNG "Wireframe")

I made sure to add edge loops so that edges remained after smoothing.

![Sideview](/media/ex4_side.PNG "Side view")
![Smoothed](/media/ex4_smooth_preview.PNG "Smoothed view")

I plan on using separate models to create handles for the doors (screw doing the topology for that with one object), and going back and using more edge loops and extrusions to create all the fun ridges on the object.