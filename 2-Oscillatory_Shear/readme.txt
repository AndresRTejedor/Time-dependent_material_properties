In order to run NEMD simulations and compute viscosity through OS one needs the following files:

LAMMPS script: LJ_lammps_wiggle.lmp
Configuration file: lj_chains_cubeT*_$F.data (./Data directory)

We have included three data files for three different temperatures at the corresponding bulk conditions. 
The LAMMPS script has the following variables:
   -Temperature (line 8)
   -Timestep (line 9)
   -Oscillation period in simulation units (line 42)
   -Deformation amplitude in box units (line 43)

To run in serial one should execute this: ./lmp_serial -i LJ_lammps_wiggle.lmp -v F N50NC375

To calculate the viscosity on should
  1. Run different frequencies for a given amplitude. 
  2. Fit the data obtain in file sig_xy.gt to Eq. (8) of the manuscript
  3. Get the values of G' and G'' from Eqs. (9-10)
  4. Take the limit in Eq. (11)
