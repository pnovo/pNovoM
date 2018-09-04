
The pNovoM software currently can only be run by command line.
Three steps to use the pNovoM: 1. Sequencing the trypsin and LysargiNase spectra (pNovo); 2. Finding mirror spectra pairs in the two sequencing result sets (pMerge); 3. De novo the mirror spectra pairs (pNovoM).
A simple example is provided. There are two mgf files of trypsin and LysargiNase, and two txt files of which are the sequencing results of those mgf files.
Input pMerge.exe param_MergeMirror.txt in command line and wait for processing. When finish, two mgf files named “output_trypsin.mgf” and “output_LysargiNase.mgf” will be generated. The number of spectra in these two mgf files is equal, spectra in the same place are mirror pairs. Then input pNovoM.exe param_deNovoMirror.txt in command line, after a few hours, pNovoM will generate a result file named denovo_results.txt. 
