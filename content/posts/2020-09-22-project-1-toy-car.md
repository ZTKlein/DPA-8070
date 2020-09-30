---
template: post
title: "Project 1:  Modeling a toy car"
slug: pr-1-car
draft: false
date: 2020-09-23T22:40:47.346Z
description: For our first project, we had to model an object in detail based on a real reference.
category: Projects
tags:
  - projects
---
## Problem:

For our first project, we had to model an object in detail based on a real reference.

## Solution:

For the project, I grabbed a $1 hot wheels toy from Target. Here's the reference photos I took of it.

![Front reference](/media/pr1_front_reference.jpg "Front reference")
![Back reference](/media/pr1_back_reference.jpg "Back reference")
![Side reference](/media/pr1_side_reference.jpg "Side reference")
![3/4ths reference](/media/pr1_34ths_reference.jpg "3/4ths reference")
![Top reference](/media/pr1_top_reference.jpg "Top reference")

I set up image planes in Maya for use with the orthogonal views, and added the images to a reference layer so that they wouldn't be selectable (Note:  the images in this picture are not the ones I used as references; this screenshot was with old references that I failed to realize were at angles and would not line up).

![References](/media/pr1_references.png "Reference setup")

I started with the side of the car, using a pipe and deleting unused faces to get a basis for the housing where the wheels go. From there I made use of a lot of edge extrusions extrusions, welds, cuts, and vertex manipulations to build out the side of the vehicle.

![Side frame](/media/pr1_frame.png "Side frame")

I moved on to build out the top, back, and front of the vehicle, eventually making use of extrusions to add depth to certain components, and the circularize tool to manipulate vertices so that I could extrude out a little pin that is on the top of the vehicle. When it came time to do the headlights, I used a boolean to push one in, and then used the cutting tool to fix the mess that was inevitably made, ensuring the surrounding geometry was still quads.

![Booleans](/media/pr1_headlight.png "Boolean headlight")

One of the last things I did was close up the bottom of the vehicle, so that I had a closed mesh At this point, I needed to get the project done, so I settled for a rather rudimentary set of extrusions to get the engine block done, and I quickly modeled some wheels on axes and used booleans to put them in place. Along with this, I ensured that the edge of the vehicle all lined up at 0 on the x axis, and finally mirrored the vehicle.

![Wireframe](/media/pr1_wireframe.png "Wireframe")
![Front view](/media/pr1_front.png "Front view")
![Back view](/media/pr1_back.png "Back view")
![Side view](/media/pr1_side.png "Side view")
![Top view](/media/pr1_34ths.png "3/4ths view")

