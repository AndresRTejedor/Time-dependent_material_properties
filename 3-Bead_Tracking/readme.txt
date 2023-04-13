In order to run NVT simulations and compute viscosity through BT one needs the following files:

LAMMPS script: LJ_lammps_bt.lmp
Configuration file: lj_chains_cubeT*_$F_N${N}R${R}.data (./Data directory)

We have included data files for three different temperatures at the corresponding bulk conditions with an embeded bead equilibrated for different radii as indicated
The LAMMPS script has the variables:
  -Temperature of the system (line 8)
  -Radius of the probe bead (line 9)
  -Number of probe beads (line 10, this should be 1 bead)

To run in serial one should execute this: ./lmp_serial -i LJ_lammps_bt.lmp -v F N50NC375

The viscosity is calculated from the MSD of the probe bead. The trajectory of such atom is in the Track_beads$F_N${N}_R${R}.lammpstrj file.
The viscosity is then calculated from the diffusion using Eq. (13) in the manuscript