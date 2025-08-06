Author Abhishek Dubasi
# Crown Gear Matching: A Cylindrical Pinion with Sine Tooth Profile

This repository presents a simulation-based design of a crown gear mechanism employing a sinusoidal tooth profile. The project explores advanced nonlinear gear meshing principles and demonstrates the practical integration of parametric modeling techniques for additive manufacturing.

## Project Overview

The objective was to model and simulate a crown gear pair where a cylindrical pinion meshes with a crown wheel using a sine-wave-based tooth profile. The design adheres to key geometric constraints including contact ratio, clearance, and backlash minimization, while ensuring interference-free engagement throughout the rotation.

## Methodology

- Parametric modeling implemented in Lua to generate sinusoidal gear tooth profiles.
- Based on the theoretical framework from *"Meshing Property Analysis of the New Sine Gears" (Wang et al., 2011)*.
- Incorporates mathematical formulations for pressure angle optimization and contact pattern stability.
- Tooth shape generation integrates additive manufacturability considerations, including overhang reduction and support minimization.

## Features

- Full 3D simulation of gear-pinion assembly with shaft alignment and rotational synchronization.
- Code is abstracted to retain core IP while enabling reproducibility of sinusoidal profiles.
- STL exports excluded due to size limits; available on request.
- Designed for fabrication using FDM or SLA 3D printing methods.

## Repository Structure

- `Crown Gear Lua Support`: Contains the Lua source code for profile generation.
- `3D view of the Design`: Includes CAD-ready model files and assembly diagrams.
- `.gitattributes`, `.gitignore`: Version control setup and file exclusions.

## Author

Abhishek Dubasi  
[Abhishek_GitHub_Projects](https://github.com/AbhishekDubasi09)
[LinkedIn Profile](https://www.linkedin.com/in/abhishek-dubasi-1051661b7/)
For additional technical queries about this design, feel free to reach out via GitHub or email.
