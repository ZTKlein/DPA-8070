---
template: post
title: "Exercise 2:  Lemon Squeezer"
slug: ex-2-lemon-squeezer
draft: false
date: 2020-09-03T03:33:47.707Z
description: For our second modeling exercise, we had to model a lemon squeezer.
category: Exercises
tags:
  - exercises
---
## Problem:

Model a lemon squeezer.

## Solution:

The start of this project was rather simple -- I created a cylinder primitive, and made sure to add rings along the top using multicut so that I could extrude downwards. I put edge loops along the edges to avoid issues when smoothing, and I added a circle around the center so that I could work with quads instead of triangles for manipulations. After extruding down, I was able to select the center and drag it back up, creating the center part of the lemon squeezer. From here I pushed in edges to create the ridges.

From the top view you can see how I handled creation of extra loops for extrusions and manipulations.

![Top raw](/media/ex2_top_raw_pre_catmull.PNG "Raw top view")
![Top closeup](/media/ex2_squeezer_closeup.PNG "Closeup view of center")

Here's how it turned out in perspective:

![Perspective Pre-Catmull](/media/ex2_perspective_raw_pre_catmull.PNG "Perspective view raw")

Using the smooth preview, I was pretty happy with how the center looked.

![Smooth pre-catmull](/media/ex2_smooth_nolip.PNG "Smoothed base")

Slight issue:  there weren't enough vertices to get a lip with nearly the fidelity I'd like. As such was the case, I figured I'd go ahead and apply catmull-clark subdivision for smoothing (2 levels, similar to what the preview provides)

Once this was done, I was able to pull out a lip on one side. Pre-smoothed final results:

![Wireframe top view](/media/ex2_top_raw_mesh.PNG "Top view wireframe")
![Wireframe persp view](/media/ex2_perspective_raw_wireframe.PNG "Perspective wireframe")

And this is what everything looks like in the end smoothed:

![Top view](/media/ex2_top_smooth.PNG "Top view")
![Perspective view](/media/ex2_smooth_perspective.PNG "Perspective view")