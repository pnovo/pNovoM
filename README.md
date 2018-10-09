## Introduction
pNovoM is a novel algorithm for de novo sequencing based on mirror peptide pair. The mirror peptide pair is defined as two peptides of the form A1A2...Al[K/R/-] and [K/R/-]A1A2...Al from trypsin and LysargiNase digestion, respectively, in which Ai denotes any one of the 20 amino acids, and "-" denotes the absence of amino acids. Nearly all of these mirror pairs contain complete product ions, resulting in precise, full-length peptide de novo sequencing.

pNovoM has the following features:

1. It can suport trypsin and LysargiNase spectra pairs.

2. Nearly all spectra pairs have full-complete fragment ions.

3. It can precisely sequence longer peptides than other algorithms.

4. It can effectively discriminate the first two amino acids.

5. It can support HCD and ETD spectra pairs.

6. It can support four spectra for each peptide: trypsin-HCD, trypsin-ETD, LysargiNase-HCD and LysargiNase-ETD.
![image](https://github.com/pnovo/pNovoM/blob/pNovoM/pNovoM.PNG)
<p><b>Figure 1.</b> Mirror protease strategy for novel de novo sequencing. <b>(a)</b> The mirror spectra improved the quality of the matched peptide-spectrum pairs by providing a complete set of fragment ions and recognizable directions of most ions (marked with blue circles, e.g., vertices 2, 3, 4 and 5). Two dotted peaks denote that b1 and y6 were missing in the trypsin spectrum. <b>(b)</b> Workflow of the pNovoM algorithm based on the mirror protease strategy for de novo sequencing. Mirror spectrum pairs from trypsin- and Ac-LysargiNase-digested samples were found and twinned using pNovoM. Then, the two spectra in each pair were merged into one spectrum graph.</p>

The pNovoM software currently can only be run by command line.

Three steps to use the pNovoM: 
1. Sequencing the trypsin and LysargiNase spectra (pNovo).

2. Finding mirror spectra pairs in the two sequencing result sets (pMerge).

3. De novo the mirror spectra pairs (pNovoM).

## Example
A simple example is provided. 

<div align="center">
  <img src="https://github.com/pnovo/pNovoM/blob/pNovoM/pMerge.jpg">
  </div>
  <p><b>Figure 2.</b>Input pMerge.exe param_MergeMirror.txt in command line and wait for processing. When finish, two mgf files named “output_trypsin.mgf” and “output_LysargiNase.mgf” will be generated. The spectra in these mgf files are mirror pairs.</p>

<div align="center">
  <img src="https://github.com/pnovo/pNovoM/blob/pNovoM/pNovoM1.jpg">
  </div>
  <p><b>Figure 3.</b>Set the mirror mgf path in param_deNovoMirror.txt, and input pNovoM.exe param_deNovoMirror.txt, pNovoM will begin to de novo the mirror pairs. </p>

<div align="center">
  <img src="https://github.com/pnovo/pNovoM/blob/pNovoM/pNovoM2.jpg">
  </div>
  <p><b>Figure 4.</b>After processing, pNovoM will generate a result filt named denovo_result.txt.</p>

## Downloads

pNovoM is currently free to use. **[Download pNovoM.](http://pfind.ict.ac.cn/software/pNovoM/index.html)**

Notice: Please read carefully the **[pNovoM Software License Agreement](http://pfind.ict.ac.cn/software/pNovoM/License.pdf)** before downloading and using the software. Please fill in the registered table and email it to pnovo@ict.ac.cn to get the registration key.

If you have any question about it, please contact pnovo@ict.ac.cn.

## pNovoM Release Notes

#### Version 1.0
* The first released version.

