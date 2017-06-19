# Tutorial for metaModules Galaxy Workflow
This is the tutorial to guide you to deploy the Galaxy workflo for metaModules, which is a recently developed metatranscriptomics computational workflow to automate identification of key functional differences between health- and disease-associated microbiomes.

This is tutorial is prepared based on the evaluated [MSc tutorial](https://github.com/ibivu/metaModules-Galaxy-Workflow) for the course "[Bioinformatics for Translational Medicine](https://goo.gl/ggXp12)" at Free University Amsterdam (Vrije Universiteit Amsterdam).

## Overview of the workflow in Galaxy
![Visualisation of the workflow](https://github.com/ibivu/metaModules-Galaxy-Workflow/blob/master/pics/metaModules_Galaxy.png)

## Galaxy tools

To deploy this Galaxy workflow, please make sure the three following Galaxy tools are properly installed in your Galaxy instance.
1. A modified DESeq2 (from Toolshed)
2. BUM model tool (from here, this tool will be published in Toolshed soon.)
3. Heinz score tool (from here, this tool will be published in Toolshed soon.)
4. Heinz optimal maximum-scoring subnetworks tool (from here)

### Why won't some tools be pushed in Toolshed?
Heinz optimal maximum-scoring subnetworks tool are using IBM ILOG CPLEX Optimizer, which is proprietary (though it is free for academics) and therefore blocks the free distribution in Toolshed. We plan to use the open source alternative to CPLEX in Heinz in the future.

Currently, you need to compile the Heinz source code yourself after you get the license of CPLEX, here we will help you create the Heinz tool step by step from Heinz source code to the two Heinz Galaxy tool.
