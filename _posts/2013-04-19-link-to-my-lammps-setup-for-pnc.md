---
layout: post
title: "link to my lammps setup for PNC"
description: "perfect version so far"
category: Molecular Dynamics
tags: [lammps, coarse grain, polymer, pnc]
---
{% include JB/setup %}

Instructions... I am too tired to type it out, just read the README, cheers.

---

**[Download](https://github.com/scottie33/amorphous_polymer_lammps/archive/master.zip)** (*Updated April 21st, 2013*)

[README](https://github.com/scottie33/amorphous_polymer_lammps/blob/master/README)

---

New stuff added: (*Updated April 21st, 2013*)

Contacts of Polymer-Polymer, Polymer-Nanoparticle, Nanoparticle-Nanoparticle.

**[CLI](http://en.wikipedia.org/wiki/Command-line_interface)** usage: **contact.bash** your.psf your.dcd residfrom residto residfrom residto sigma1 sigma2

*e.g.*

	contact.bash my.psf my.dcd 1 64 65 65 4.7 6.1

in the above example, **resid 1 to 64** are polymers, they will be chosen as the 1st selection for [VMD](http://www.ks.uiuc.edu/Research/vmd/), **resid 65**, the particle, the 2nd selection, and **4.7, 6.1** are the pair_coeff sigmas for polymer and nanoparticle respectively in the system we set up. At last you will have a contact evolution figure with respect to the timestep (system unit). Hope you can understand this poor instruction...

Here is a simple result, yes, you will see this kind of figure after the command run (this one is from a very short trajectory, since it's 3 am, I don't want to wait for a long trajectory to be hacked).

----

![an contact example](/images/2013/April/21/Contacts.png "an contact example")

-----

By the way, it's a little bit slow by far, depending on the size of your system and the length of the trajectory (timestep unit), I am focusing on it trying to optimize its performance, accelerating is always good, high-way drivers.

Have fun, Cheers.

---

![an rdf example](/images/2013/April/21/grdf.png "an rdf example")

----
