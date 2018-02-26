---
layout: post
title: VR Property Data Inspector
[comment]: <> (Unity3D, UTC Vive, C# -)
---

[comment]: <> (VR Property Demo)
<iframe width="560" height="420" src="http://www.youtube.com/embed/dHYoUD4EKs4"></iframe>

This project explores the potiental of displaying property information in a 3D medium.
 
The property information starts in a JSON format.

A parser reads and decrypts the information to be displayed in a more understandable format.

This involves converting a set of 2D points in geoJSON that defines the bounds of certain elements of the property into 3D.

This is drawn in Unity3D as a custom mesh.

Mapbox is also used and queried to obtain surrounding map information of the property.

Virtual Reality interactions were added in order to have additional context to the information of the property.

The Key elements I worked on were the custom mesh drawing, the 3D Shaders for transparency/opacity switching and the VR controls and interaction.



