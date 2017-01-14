---
layout: post
title:  "Seasonal Snowglobe"
date:   2012-08-02 00:00:00 +0000
permalink: /snowglobe/
categories: portfolio
---
[![YT Seasonal Snowglobe](https://img.youtube.com/vi/LipQ68PPCio/0.jpg)](https://www.youtube.com/watch?v=LipQ68PPCio)

As part of the MEng in Computer Science with Games Development course at the University of Hull we were required to develop a simulation of a seasonal snowglobe with the following features:
* A fractal tree with leaves that fall to the ground in autumn
* Particle systems for snow, fire and smoke effects
* Reflective pond surface
* Directional and spot lighting

We were required to use OpenGL and GXBase (a context creation wrapper), but were not restricted to a particular subset of the OpenGL API. I decided to restrict myself to the OpenGL 3.0 API which required me to replace many of the fixed function pipeline features I had relied on on previous OpenGL projects. In total we had around two months to work on the project alongside other university work. After a couple of weeks setting up a set of classes to simplify the use of OpenGL I spent the majority of the remaining time developing the fractal tree and various particle systems.

I developed an L-System language for representing trees. My simple language includes commands for emitting branches, rotation, scaling and modifying the stack. Using these simple rules I have been able to generate trees in the style of various species.

[![Snowglobe 1](/download/thumbnail.tree1.png)](/download/tree1.png)
[![Snowglobe 2](/download/thumbnail.tree2.png)](/download/tree2.png)
[![Snowglobe 3](/download/thumbnail.tree3.png)](/download/tree3.png)

In previous projects I have implemented various particle systems on both the CPU and GPU. In this project I decided to implement the particle effectsentirely in vertex shaders. There are various approaches to implementing particle systems in shader, I decided to implement particle systems statelessly. In this approach each particle can be described by a function of it's ID and time, which has the advantage of zero memory footprint per particle.

[![Snowglobe 4](/download/thumbnail.tree4.png)](/download/tree4.png)
[![Snowglobe 5](/download/thumbnail.tree5.png)](/download/tree5.png)
