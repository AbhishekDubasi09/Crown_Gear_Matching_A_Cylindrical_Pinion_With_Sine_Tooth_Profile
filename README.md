# Crown gear with a sine-profile pinion

A crown gear driven by a cylindrical pinion whose teeth follow a sine curve, designed with parametric scripting in Lua and
meant to be 3D printed (FDM or SLA). It is a simulation-based design: the geometry was generated and assembled in software,
and the printable parts were exported as STL files.

## The design

A crown gear has its teeth on the face of a disc, and a cylindrical pinion meshes with it, usually at a right angle. Here the
pinion's tooth profile is a sine curve instead of the usual involute. The design targets these properties:

- a suitable contact ratio
- enough clearance and minimal backlash
- no interference between the teeth through the full rotation
- a tooth shape that prints without much support material (limited overhang)

The tooth profile follows the sine-gear approach in *"Meshing Property Analysis of the New Sine Gears"* (Wang et al., 2011).
The design also uses formulations for pressure angle optimisation and for the stability of the contact pattern.

## How the geometry is generated

The generator is a parametric script. In outline:

1. **Pinion.** Build the sine-modulated tooth profile from the module, the number of pinion teeth, the width and the crown
   diameter: sweep the angle, compute the radius from the sine function, store the profile points, extrude them and subtract
   the mounting bore.
2. **Crown base.** Build the disc from the inner and outer radii, with a central mounting hole.
3. **Crown teeth.** Cut the crown by rotating the pinion step by step and subtracting it from the base, so the crown teeth take
   the shape the pinion sweeps out.
4. **Full crown.** Repeat the cut sector around the full 360 degrees and merge it.
5. **Mechanism.** Add the shafts, holders, grooves and stops, and modular blocks such as plates, with boolean operations.

The script has four views: a simplified view (crown and pinion only), the assembled mechanism, an exploded view, and a single
tooth sector with its base.

The exported parts include the crown gear, the sine pinion, a support for each, the pinion handle, the crown stopper, and a worm
shaft with its support.

## What is not in this repository

- The STL files, which are more than 200 MB in total. They are available on request.
- The full Lua script. The outline above is a general summary of it.
- No open-source licence is attached to the design or the script. If you want to use or reproduce them, please contact me.

## Further reading

- Wang et al. (2011), *Meshing Property Analysis of the New Sine Gears*, as cited above.
- [Sinusoidal Gears and Alternative Method of Tooth Generation](https://link.springer.com/chapter/10.1007/978-3-030-92262-7_8),
  Springer.

## Author

Abhishek Dubasi, [GitHub](https://github.com/AbhishekDubasi09),
[LinkedIn](https://www.linkedin.com/in/abhishek-dubasi-1051661b7/). For questions about the design, write to me through
either of these.
