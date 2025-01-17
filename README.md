# Digital-Spatial-Profiling-Workflow Test Development Version

Demo CD 2/8/2024 1054
test 2/13

The DSP Workflow addresses a growing need to streamline the analysis of Spatial Transcriptomics data produced from Digital Spatial Profiling Technology (NanoString). It can be run in a docker container, and for biologists, in user-friendly web-based interactive notebooks (NIDAP, Palantir Foundry). It is based on the Bioconductor vignette ["Analyzing GeoMx-NGS RNA Expression Data with GeomxTools
"](http://bioconductor.org/packages/release/workflows/vignettes/GeoMxWorkflows/inst/doc/GeomxTools_RNA-NGS_Analysis.html).  

It has been tested on several Whole Transcriptome Atlas (WTA) [human](https://nanostring.com/products/geomx-digital-spatial-profiler/geomx-rna-assays/geomx-whole-transcriptome-atlas/) and [mouse](https://nanostring.com/products/geomx-digital-spatial-profiler/geomx-rna-assays/geomx-mouse-whole-transcriptome-atlas/) datasets. The workflow can be summarized in these steps:
<img src="./vignettes/workflow_image.png">


Future development will include support for [protein data](https://bioconductor.org/packages/release/bioc/vignettes/GeomxTools/inst/doc/Protein_in_GeomxTools.html) and integration with single cell datasets.


The development environment is provided in the Dockerfile/ directory, there are two sets of files:
  1. Conda_container/ : The container includes a conda environment: DSPWorkflow_NDIAP.
  2. Plain_R_container/ : Then container includes a plain R environment.
