# Guideline for Galaxy tools
The Galaxy workflow is based on metaModules (Ali May et al, 2016), consisting of four major Galaxy tools, which are in four subdirectories here.

1. `deseq2`: A modified DESeq2, if you installed Deseq2 from Toolshed, please replace deseq2.R with the modified version in this folder.
2. `bionet`: BUM model tool (this tool will be published in Toolshed soon.)
3. `scoring`: Heinz score tool (this tool will be published in Toolshed soon.)
4. `heinz`: Heinz optimal maximum-scoring subnetworks tool. In this folder, the execution file 'heinz' is a fake one, you need to follow the guide below to generate yours by compiling the Heinz source code after you have got the legal copy of CPLEX.

## Manual installation

Manual installation of Galaxy tools is straightforward, please follow the [official guide]([here](https://galaxyproject.org/admin/tools/add-tool-tutorial/)) for more details.

1. Put the tool directory (one of the four directories here) into Galaxy server path e.g.`tools`.
2. Modified `tool_conf.xml` to point to the xml file.

3. For Heinz optimal maximum-scoring subnetworks tool, please follow the guideline below to compile the source code of Heinz first to generate 'heinz' file, the replace the fake file with this one. Then please follow Step 1 and 2 to finish the installation.

## Obtain the real `heinz` file

NB: in the heinz folder, `heinz` is a fake file. Please obtain the real one to replace this fake one before you install this tool into Galaxy.

1. You need to get the license of IBM ILOG CPLEX Optimizer first. The academic license is free. Please download and install IBM ILOG CPLEX Optimizer. The version should be no below 12.0.
2. Install [lemon 1.3.1](https://lemon.cs.elte.hu/trac/lemon) and [OGDF 201207](https://github.com/ogdf/ogdf) separately.
  * You can install them using the source code, please follow the tutorial [here](https://github.com/ls-cwi/heinz/blob/master/README.md).
  * Alternatively, we recommend installing them from Anaconda.[lemon](https://anaconda.org/conda-forge/lemon) [OGDF](https://anaconda.org/bioconda/ogdf)
