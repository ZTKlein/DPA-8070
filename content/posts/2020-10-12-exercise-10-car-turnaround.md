---
template: post
title: "Exercise 10:  Toy Car Render"
slug: ex10-render
draft: false
date: 2020-10-12T00:39:58.137Z
description: For exercise 10, we had to revisit project 1 and 
category: Exercises
tags:
  - exercises
---
## Problem:

Make project 1 look good and do a turnaround.

## Solution:

To start, I worked on making shaders for different parts of the car. I used 7 shaders total for this, with the most effort put into the car paint shader used for the chassis.

![Node graph](/media/ex10_nodeGraph.png "Hypershade graph")

Most of the nodes are Arnold standard surfaces, but the car paint is an Arnold car paint node, which has some extra controls just for the task. Here's the properties I used for it.

![Car Paint](/media/ex10_paintProperty.png "Car paint")

You'll notice that there's some flip-flop properties -- those affect how light is reflected based on the viewing angle, and these were connected to color ramps. Here's the specular and flake ramps.

![Specular ramp](/media/ex10_specularFlipFlop.png "Specular flip-flop")
![Flake ramp](/media/ex10_flakeFlipFlop.png "Flake flip-flop")

For the lighting, I used the free fluorescent blaze HDRI from https://www.poliigon.com.

![HDRI](/media/ex10_HDRI.png "HDRI")

I set up a turnaround for 120 frames, because 90 felt a bit short. Even with 120, I didn't do a full 360 degree turnaround.

Initially, I did a test render and rendered out AOVs at 1920x1080. I used the AOV's to figure out that there was noise in the diffuse and specular, and upped the camera samples there to 2 and 2, as well as enabling adaptive sampling. Unfortunately, I also discovered that it would take far too long to render out everything at this quality, so I had to bump down the resolution to the HD_540 preset (960 x 540). Simply put, I can't afford to put my desktop out of commission for more than a day, and I'm not aware of how to use the DPA pipeline yet to do renders using the school machines. Even with these settings, it took my desktop around 20 hours to render out the sequence.

Unfortunately, it looks like without doing a higher quality render, the subtle details added from paint flakes aren't visible, which is a real shame -- I spent a lot of time trying to get that to look good when I was doing test renders.

Once all this was done, I loaded the sequence into Premiere, and here's the video.

<video width="960" height="540" controls>
  <source src="/media/ex10_toy_car_turnaround.mp4" type="video/mp4">
</video>