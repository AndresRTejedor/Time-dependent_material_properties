# Time-dependent_material_properties
Supporting code and Data for the Paper of Tejedor et al entitled "Time-dependent material properties of ageing biomolecular condensates from different viscoelasticity measurements in molecular dynamics simulations"

Here we include the code necessary to apply the methods presented in our work paper.

The majority of the code requires a compiled version of Lammps. We used the 21 July 2020 version for these calculations running on Linux (kernel 3.10.0) with standard libraries. There are seven directories in this archive. We inlcude three different direcotories corresponding to each computational method to measure viscosity using the LJ system (Fig. 1)

################ LAMMPS ################ Instructions on how to compile Lammps are provided at https://docs.lammps.org/Build_make.html.

1- In a clean directory, download the last version of Lammps (https://www.lammps.org/download.html) 
2- Compile the following packages first: 
  a) 'make yes-USER-MISC' (To calculate viscosity through GK) 
  b) 'make yes-MOLECULE' (Model molecular systems) 
3- Compile lammps with 'make mpi' or 'make serial' depending on whether parallelisation is desired. 4- Copy the resulting executable file (lmp_serial or lmp_mpi) to the desired directory with all the files required to run the simulations. 5. Run the simulation. ./lmp_serial -i input-script.dat
