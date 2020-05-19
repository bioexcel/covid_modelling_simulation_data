Structure models of the SARS-CoV2 RNA directed RNA polymerase (RdRp) or nsp12 in complex with two nsp8 proteins and one nsp7 protein. The models are built using homology modelling with the SARS-CoV-1 RdRp complex (PDB:6NUR) as template structure (https://doi.org/10.1038/s41467-019-10280-3). The generated structure models have been validated by fitting and comparing conserved interactions with recently published SAR-CoV2 RdRp structures (PDB: 6M71, 7BTF, 7BV1, 7BV2, 6YYT).

Each model describes a different RdRp complex system:
1) apo-RdRp: apo-protien model of RdRp complex 

2) RdRp-RNA-ATP-complex: RdRp apo-protein in complex with RNA template-primer strands and non-covalently bound ATP molecule

3) RdRp-RNA-RTP-complex: RdRp apo-protein in complex with RNA template-primer strands and non-covalently bound active form of Remdesivir (RTP) molecule in tri-phosphate form.

The fitted models have been equilibriated to perform long MD simulations.  

To use it you need Gromacs 2018.8 or better installed. 

AMBER14sb forcefields parameters for ATP were extrcated from the AMBER parameters database shared by Bryce Group (http://research.bmh.manchester.ac.uk/bryce/amber/). The parameters for the tri-phosphate form of Remdesivir molecule RTP molecules were derived using the same approach used for generating AMBER parameters for RNA base pairs.

You can lookup the detials MD parameters in grompp.mdp and in the Gromacs manual (http://manual.gromacs.org/documentation/2018/user-guide/mdp-options.html)

To compile your own tpr simulation file use the following command in the corresponding derectory of the model:

gmx(_mpi) grompp -f grompp.mdp -p topol.top -c conf.gro -n index.ndx -o yoursimulation.tpr