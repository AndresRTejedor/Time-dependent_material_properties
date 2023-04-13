In order to run NVT simulations and compute viscosity through GK one needs the following files:

LAMMPS script: LJ_lammps.lmp
Configuration file: lj_chains_cubeT*_$F.data (./Data directory)

We have included three data files for three different temperatures at the corresponding bulk conditions. The LAMMPS script has a variable
in line 8 for the system temperature

To run in serial one should execute this: ./lmp_serial -i LJ_lammps.lmp -v F N50NC375

The viscosity is calculated from the Gt$F_T${T}.gt file following equation (4) and (5) in the manuscript