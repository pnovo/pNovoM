pNovoM软件，目前没有软件界面，只能使用cmd命令行方式运行。
pNovoM软件分三步：1. 使用pNovo软件先对trypsin和LysargiNase数据集分别进行从头测序 (pNovo)；2. 在两组结果中查找可能成镜像的谱图对 (pMerge)；3. 使用pNovoM对镜像谱图对从头测序 (pNovoM)。

该路径下有一个简单的例子，在Example文件夹下，两个mgf文件，分别对应trypsin和LysargiNase数据集的谱图，两个txt文件，分别对应已经使用pNovo软件对这两组数据集从头测序的结果。
第二步：在本路径上输入"cmd"命令，弹出命令行窗口，在窗口中输入"pMerge.exe param_MergeMirror.txt"命令，进行运行，这部分可能需要几个G的内存，所以建议在服务器上运行，根据数据集的大小，约运行几十分钟出来结果。运行完后会在该路径下出现两个mgf文件，名字分别是"output_trypsin.mgf"和"output_LysargiNase.mgf"，这两个mgf的谱图数量一致，两两互为一对镜像谱图对。
第三步：仍然在命令行窗口上输入新的命令"pNovoM.exe param_deNovoMirror.txt"命令，对"output_trypsin.mgf"和"output_LysargiNase.mgf"进行镜像的从头测序，大概需要数小时后，出来结果，生成一个"denovo_results.txt"的文本文件。