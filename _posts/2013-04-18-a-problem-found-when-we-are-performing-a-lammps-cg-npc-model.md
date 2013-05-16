---
layout: post
title: "A problem found when we are performing a lammps CG NPC model"
description: "a tiny teeny ignorance wastes months' or even years' effort"
category: Molecular Dynamics
tags: [lammps, coarse grain, polymer, pnc]
---
{% include JB/setup %}

### The problem
When we decide to explore the **[Radius Distribution Function](http://en.wikipedia.org/wiki/Radial_distribution_function)** (**RDF**) of our **NanoParticle Polymermatrix Composite** (**NPC)** system, we found that there is a peak around *R*=0.0 (in angstrom), which is impossible since in our model the interaction coefficients are set to prevent 'atom's from approaching each other closer than ~4.0.

After checking the trajectories with **[Visual Molecular Dynamics](http://www.ks.uiuc.edu/Research/vmd/)** (**VMD**), we found that 'atom's were able to get as close as 0.0 to their 'second neighbor', in almost every frame. Given this phenomenon is physically unreal and directly results to the RDF unusual peak we found, we thought it was more or less the reason, and it might be caused by the implicit shutdown of 1-3 interaction between particles in **[lammps](http://lammps.sandia.gov)**.

### Why
In lammps, or some of other **[Molecular Dynamics](http://en.wikipedia.org/wiki/Molecular_dynamics)** (**MD**) softwares, the 1-3 and 1-4 interactions are implicitly ignored. The contributions of 1-3 and 1-4 interactions are normally considered included in angle- and dihedral- calculations respectively, inherently due to the way we extract angle- and dihedral- coeffients from experients data and artificial method. In our model, we consider no angle- and diheral- interactions at all, though tragedily, forgot to explicitly tell lammps we need to have 1-3 and 1-4 interactions calculated to mimic the real physical world.

### How-to fix it
We add the following line into the .in file for lammps to fix this problem:

    special_bonds fene angle no dihedral no
or
    
    special_bonds lj 0.0 1.0 1.0

It just runs fine now and produces a reasonable result.