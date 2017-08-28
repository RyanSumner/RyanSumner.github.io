---
layout: post
title: Fire Particles
[comment]: <> (C++, OpenGL -)
---

![_config.yml]({{ site.baseurl }}/gifs/FireParticles.gif)

A project exploring the use of a particle system for a final assignment during University.

One particle emitter that spawns a number of particles with a random lifespan (within a range) and random velocity. 
The colour of a particle changes proportionally to its lifespan, having a blue/white colour with a high lifespan changing to orange then red over time.
All the particles have a force acting on them to drive them upwards and towards the centre of the screen.

This project was programmed in C++ using OpenGL inside Visual Studio, using external dependencies such as the glut and glaux libraries.

The source files can be found [here](../downloads/FireParticles.zip)