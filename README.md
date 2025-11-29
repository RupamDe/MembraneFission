# MembraneFission

## Input_files

This directory contains .gro files of the last frame of the trajectory, .top files and .mdp files corrsponding to various systems.

#### Command to generate cylindrical tube from flat membrane using BUMPY:

_python2 bumpy.py -f flat-dope.pdb -s cylinder -z 8.3 -g r_cylinder:40 l_cylinder:300 -o dope-cyl.pdb -p topol.top -n index.ndx_

Here, r_cylinder and l_cylinder indicates the radius and length of the cylinderical tube (in angstrom) repectively. -z is to set the location of the pivotal plane (ref. 1) at 8.3 (for DOPE) angstrom, -s is to set gerometry of the flat membrane (flat_dope.pdb) as a cylinder.


## Umbrella_sampling

This directory contains plumed.dat file to generate different stages of fusion process. Given files are for fission in 4 nm cylindrical tube with scission region width of 2 nm indicated by "ZUPPER" and "ZLOWER" (upper and lower limit around DM bead by specifying the index of DM in "AROUND ATOM"). "DENSITY SPECIES" (in plumed.dat) contails the index number of all carbon beads (mentioned in the main text) of lipid molecules.


## References

1. Boyd, Kevin J., and Eric R. May. "BUMPy: a model-independent tool for constructing lipid bilayers of varying curvature and composition." Journal of chemical theory and computation 14.12 (2018): 6642-6652.
