MEDOC_public
Public release of the MEDOC algorithm for the prediction of protein protonation states MEDOC necessitates a high precision python3 (64bits) environment to work on larger sequences.

To use MEDOC, open a terminal and type : python3 MEDOC_V1.0.py [command line arguments]
The following command line arguments can be specified to change the default behavior.
-nn int Number of neighbors. Default is 2.
-dl int Detail level for figure and message printing. 0 is no figure, 1 adds the net charge vs pH plot and the charge density vs pH (if site specific is on) , 2 adds the mesostate plot and the plot of all sites protonation curve for all residue types at once, 3 adds the separate site specific curves for each amino acid type (if site specific is on) 4 adds a figure for each protonation sites with an analysis of the cooperativity and transition asymmetry (if site-specific is on).
-pr float Plots resolution in the pH space. Default is 0.01. Greatly affects figure printing speed, but has no effect on the speed of the algorithm itself. -t float Temperature of the calculation in Kelvin.
-pt str Prediction type. Affects the free energy used for each charge context. Can be Implicit (I) or Unshifted (U). Due to the size and non-exhaustive nature of the explicit context database, it is not available to the public.
-ss int 0 is the global prediction (default), one is the site specific prediction
-be float This is the value for the reference energy. Base value is -709*R*T. This can be changed to get around the partition function "breaking" due to exceeding max floating point value.


If the procedure does not get to the end and has an error message, this may be due to a system dependent floating point issues. Try a machine with higher precision. This was tested on a linux machine with a 64-bit  python distribution.

You will get the error message : RuntimeWarning: divide by zero encountered in log This is normal.
