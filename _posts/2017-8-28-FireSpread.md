---
layout: post
title: Fire Spread using Unity3D
---

[comment]: <> (Single Flame)
<iframe width="560" height="315" src="https://www.youtube.com/embed/lg5l6ATXPi0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This was a project I was working on during University using Unity3D. The idea was to have fire spread across a surface or object by using the vertex, edge and face data of the mesh.

A tree based data sturcture was used to keep track of vertex adjecency and what vertex and edges were 'burnt' or were 'burning'. 
This also allowed multiple fires to spread on the same mesh and behave properly. 

Some noise was added to the travel speed of the flames to decrease the linearity of the fire spread (the difference with and without the noise is shown in the videos).
Unity then handled the partical emission to make the flames themselves and Unity's colliders were used to make it possible to spread to nearby meshes.

Unfortunately the original code (written in C#) was lost and only these output videos remain.

[comment]: <> (Single Flame With Noise)
<iframe width="560" height="315" src="https://www.youtube.com/embed/pO0YtNegLyc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[comment]: <> (Two Flames)
<iframe width="560" height="315" src="https://www.youtube.com/embed/kJUhSyE1o1s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[comment]: <> (Two Flames with Noise)
<iframe width="560" height="315" src="https://www.youtube.com/embed/n_E8qFc4D4k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[comment]: <> (Multiple Objects)
<iframe width="560" height="315" src="https://www.youtube.com/embed/FZSO-QazdR8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[comment]: <> (Large Scale with Multiple Flames)
<iframe width="560" height="315" src="https://www.youtube.com/embed/-X39TfjREgI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

