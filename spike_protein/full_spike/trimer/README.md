Model of the spike protein trimer of SARS-CoV-2 virus in closed conformation. 
That trimer is built from the homology model of monomer made by Thomas Desautels et.al. (https://doi.org/10.1101/2020.04.03.024885)
It has been replicated and fitted to the known structure of SARS-CoV-1 by Wenfei Song et.al. PDBID: 6ACK (https://doi.org/10.1371/journal.ppat.1007236). 
That model has been made to perform MD simulations. 

To use it you need Gromacs 2018.8 or better installed.
CHARMM27 forcefield should be located at the /share/top/charmm27.ff inside the Gromacs directory.

You can lookup for MD parameters in grompp.mdp and in the Gromacs manual (http://manual.gromacs.org/documentation/2018/user-guide/mdp-options.html)

To compile your own tpr simulation file use the following command:

gmx(_mpi) grompp -maxwarn 10 -f grompp.mdp -p topol.top -c conf.gro -n index.ndx -o yoursimulation.tpr