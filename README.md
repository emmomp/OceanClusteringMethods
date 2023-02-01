# OceanClustering

This repositary contains python code and notebooks to accompany the manuscript "A heuristic method for detecting overfit in unsupervised classification of climate model data" Boland et al 2023 ([pre-print]()). The contents will allow for the reproduction of all figures in the paper, as well the fitting of Gaussian Mixture Models on the source data. See below for more details.

Feel free to use or reproduce the code and figures but please attribute as outlined in the license.

E Boland Feb 2023 [emmomp@bas.ac.uk](mailto:emmomp@bas.ac.uk)

## Requirements

TO COME

## Steps to reproduce the paper's figures (will over-write data in [figures/](figures/))

To reproduce the paper's figures, follow these steps:
- Clone the repository
- Install necessary libraries (see requirements above).
- Run the Figure_*.ipynb notebooks.

## Steps to fit the GMMs on the original model output (will over-write data in [model/](model/))

- Access the UK-ESM1.0 CMIP6 data archive is required, for example through the [UK CEDA archive](https://www.ceda.ac.uk/) or the [Google Cloud Archive](https://console.cloud.google.com/marketplace/product/noaa-public/cmip6)
- Install necessary libraries (see requirements above)
- Repository 
- Run the Step1_... and Step2_... notebooks

### Further details

Two forms of cluster_utils.py are provided - one that is designed for [PANGEO](https://pangeo.io/) instances that connects with the Google Cloud Archive, the other that is designed for the UK's [JASMIN](https://jasmin.ac.uk/) service which has access to the CEDA archive. 
