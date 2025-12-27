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

