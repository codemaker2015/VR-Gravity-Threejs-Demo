# VR Gravity Threejs Demo

![demo](demo/demo.gif)

A simple experiment allowing you to change gravity in VR, affecting your virtual position along with a bunch of colored balls in the room.

Change the direction of gravity by rotating your right controller while holding the trigger. If you squeeze the trigger with your controller grip aiming down at the floor, as you rotate your controller gravity will match the direction your controller grip is pointing.

The 3D scene and VR support is built with [A-Frame](https://aframe.io), which uses [three.js](https://threejs.org) for rendering, lighting, shadows, etc. 

The move and rotate of virtual camera using a custom "camera rig" that still supports free head-tracked movement, but forces the default camera/user orientation to point up relative to gravity, and float 1.6m above whatever happens to be the floor.

The 3D ball collision physics are a solved using a distance constraint and Verlet integration. This is fully implemented in this pen in under 60 lines of code. It's not perfect, and isn't the most performant solution, but makes for a fun simple demo and 50 balls runs well on a Quest 2. More powerful systems can simulate a couple hundred balls.