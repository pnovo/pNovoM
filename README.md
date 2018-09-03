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
![Image text](https://github.com/pnovo/pNovoM/pNovoM.PNG)
