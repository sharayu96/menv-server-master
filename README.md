''' THIS PROGRAM WORKS WITH UBUNTU PLATFORM ONLY !''' 

#This program calculates free energy changes based on two-state conformations.
# This ΔG calculation is based on protein microenvironment changes.
# ΔG can currently be computed for two-state conformations of the protein. For example, a protein with the same sequence but in alpha-helical and beta-sheet conformation or a protein in its free form and its ligand-bound form.
# Hence, the user should ensure that the residue numbers and names in two PDB files match; otherwise, this calculation will give wrong results
......................................................................................................................

1. Download the necessary libraries:
 a. gfortran
 b. python3 - pandas, numpy 
 c. csh
......................................................................................................................

2. It is required to activate the executable as follows:
 a. chmod +x /path/psfgen and similarly; 
 b. chmod +x /path/micro_debug_
 
3. compile the following programs using command line: 
 a. gfortran -O2 -o psfpdb-crd-conv2 psfpdb-crd-conv2.f
 b. gfortran -O2 -o ssbond.exe ssbond-detect.f
 
......................................................................................................................

# To execute the code, run the C-shell script (script4)
5. Download and store only two pdb files in the same directory (in case you have more than two PDB files, those will be merged together and produce wrong results).
6. preprocessing will be done in the next few steps
 a. The user has to change the directory names (path), as given in line 17, and subsequently change the directory names in lines 19, 20, 23, 24, 27, 33, 34, and 39 (of script4)     after downloading the files on your local machine.
 b. change the directories for the following files:
    psf-pdb-gen-standalone.tcl (line 3), newrenumber.sh (line 10, 34, 70), del_G, temp-psfgen-scripts.tcl (line 8).

.......................................................................................................................
# The ΔG calculations will be printed in a 'data.csv' file (raw data containing ΔG values for individual functional groups).
# A separate statement will pop up stating the difference between two-state conformations of the protein.
