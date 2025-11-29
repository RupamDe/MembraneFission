# MembraneFission
## Input_files
This directory contains .gro files of the last frame of the trajectory, .top files and .mdp files corrsponding to various systems.

### Command to generate the initial file using BUMPY:
python2 bumpy.py -f flat-dope.pdb -s cylinder -z 8.3 -g r_cylinder:80 l_cylinder:300 -o dope-cyl.pdb -p topol.top -n index.ndx

Here, r_cylinder and l_cylinder indicates the radius and length of the cylinderical tube (in angstrom). -z is to set the location of the pivotal plane (ref1 for details) at 8.3 (for DOPE) angstrom, -s is to set gerometry of the flat membrane (flat_dope.pdb) as a cylinder.
