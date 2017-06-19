# Guideline for Galaxy tools
The Galaxy workflow is based on metaModules (Ali May et al, 2016), consisting of four major Galaxy tools, which are in four subdirectories here.

1. `deseq2`: A modified DESeq2, if you installed Deseq2 from Toolshed, please replace deseq2.R with the modified version in this folder.
2. `bionet`: BUM model tool (this tool will be published in Toolshed soon.)
3. `scoring`: Heinz score tool (this tool will be published in Toolshed soon.)
4. `heinz`: Heinz optimal maximum-scoring subnetworks tool. In this folder, the execution file 'heinz' is a fake one, you need to follow the guide below to generate yours by compiling the Heinz source code after you have got the legal copy of CPLEX.
