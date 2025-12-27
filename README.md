# Particle_Lib
> A Particle Library for Minecraft Beet Datapack Development

---

## Introduction
This is a library for standard and modded particles for minecraft using [beet](https://github.com/mcbeet/beet) and [bolt](https://github.com/mcbeet/bolt) to prebuild the commands during built time. This library is created for datapack developers who want fast alternatives to creating geometry in minecraft. Here are some things this library can do.

- Create Lines, Circles, Squares, Spheres, Plane generation, and Complex polygons <sup>WIP</sup>.
- Able to define to world coords, relative coords, or orientated to direction an entity is looking at.
- Can specify the amount of particles an object can have.
- Hold floating and .math functions inside coords and gradient particles
- Rotate any particle object (Other than planes) along all 3 rotation axes.

## Installing
This library currently is in major works to be packaged once all features are met, the only way is to drag and drop the `particle_lib folder` into the `src/data` folder or whatever your folder path your beet.json files path loads to. Then in your .bolt file you need to run these two commands, the first command will initialize the library and the second one you can change what its equal to.

```Python
from particle_lib:plib import ParticleLibrary
particles = ParticleLibrary()
```
This will soon be changed to work like the import math once everything is finalized. 

---

<details open>

<summary>All Objects In Library:</summary>

## Object Innitializer
>This is what creates the object to later be used in rendering.

| Object  | What it Does | How to use |
| ------------- | ------------- | ------------- |
| Line3D  | This creates a line in 3D space  | To create a line you need to input x1 y1 z1 for first coords and x2 y2 z2 for second coords. Then specify the amount of particles you want to use, see the example here. |
| Circle3D  | This creates a 2D circle tied to a plane of axis  | To create a circle you need to input x1 y1 z1 for first coords and x2 y2 z2 for second coords. Input the amount of particles you use and then an axis its rotated on, allowed axes are "XZ","XY","YZ" only.  |
| Square3D  | This creates a uniform square with uniform size, aligned only to xz grid as base.   | To use this you need just x1 y1 z1 for your first set of coords, the size of the square, and finally the amount of particles in that order.|
| Circle3D  | This creates a circle in 3D space that could be filled   | To use you just need x1 y1 and z1 but also a set radius, the amount of particles, and whether it is filled or not.  |
| Plane3D  | This creates a directional plane with set radius  | All you need for this is x1 y1 z1 and x2 y2 z2 for setting up the plane, it then rotates based on connecting the two points, cannot rotate because rotation is prebuilt in.  |
| Polygon_MeshFromPoints  | This creates a 3d render of a polygon  | This one is the most buggy but how you use it is by setting up a dictionary of 3 variable tuples like [(x,y,z),(x,y,z)] and so on, then you specify the amount of particles.|
</details>

