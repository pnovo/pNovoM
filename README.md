### **Introduction**
pNovoM® is a novel algorithm for de novo sequencing based on mirror peptide pair. The mirror peptide pair is defined as two peptides of the form A1A2...Al[K/R/-] and [K/R/-]A1A2...Al from trypsin and LysargiNase digestion, respectively, in which Ai denotes any one of the 20 amino acids, and "-" denotes the absence of amino acids. Nearly all of these mirror pairs contain complete product ions, resulting in precise, full-length peptide de novo sequencing.

pNovoM not only can sequence the mirror spectra pair (one from trypsin and another from LysargiNase), but also can sequence the HCD and ETD spectra. When all four spectra: trypsin-HCD, trypsin-ETD, LysargiNase-HCD and LysargiNase-ETD are considered, the recall of pNovoM can as high as 99% on the top three candidates.

pNovoM has the following features:

1. It can suport trypsin and LysargiNase spectra pairs.

2. It can support HCD and ETD spectra pairs.

3. It can support four spectra for each peptide: trypsin-HCD, trypsin-ETD, LysargiNase-HCD and LysargiNase-ETD.

4. Nearly all spectra pairs have full-complete fragment ions.

5. It can precisely sequence longer peptides than other algorithms.

6. It can effectively discriminate the first two amino acids because of existing b1 ions.
![image](https://github.com/pnovo/pNovoM/blob/pNovoM/pNovoM.PNG)
Figure 1. Mirror protease strategy for novel de novo sequencing. (a) The mirror spectra improved the quality of the matched peptide-spectrum pairs by providing a complete set of fragment ions and recognizable directions of most ions (marked with blue circles, e.g., vertices 2, 3, 4 and 5). Two dotted peaks denote that b1 and y6 were missing in the trypsin spectrum. (b) Workflow of the pNovoM algorithm based on the mirror protease strategy for de novo sequencing. Mirror spectrum pairs from trypsin- and Ac-LysargiNase-digested samples were found and twinned using pNovoM. Then, the two spectra in each pair were merged into one spectrum graph.

The pNovoM software currently can only be run by command line.

Three steps to use the pNovoM: 
1. Sequencing the trypsin and LysargiNase spectra (pNovo).

2. Finding mirror spectra pairs in the two sequencing result sets (pMerge).

3. De novo the mirror spectra pairs (pNovoM).

A simple example is provided. There are two mgf files of trypsin and LysargiNase, and two txt files of which are the sequencing results of those mgf files.

Input **pMerge.exe param_MergeMirror.txt** in command line and wait for processing. When finish, two mgf files named “output_trypsin.mgf” and “output_LysargiNase.mgf” will be generated. The number of spectra in these two mgf files is equal, spectra in the same place are mirror pairs.

Then input **pNovoM.exe param_deNovoMirror.txt**, after a few hours, pNovoM will generate a result file named denovo_results.txt. 
