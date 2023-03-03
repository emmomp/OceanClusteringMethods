# OceanClusteringMethods
[![DOI](https://zenodo.org/badge/609181408.svg)](https://zenodo.org/badge/latestdoi/609181408)

This repositary contains python code and notebooks to accompany the manuscript "A heuristic method for detecting overfit in unsupervised classification of climate model data" Boland et al 2023 ([pre-print]()). The contents will allow for the reproduction of all figures in the paper, as well the fitting of Gaussian Mixture Models on the source data. See below for more details.

Feel free to use or reproduce the code and figures but please attribute as outlined in the license.

E Boland Mar 2023 [emmomp@bas.ac.uk](mailto:emmomp@bas.ac.uk)

## Directory Contents

- Jones2019_data: Contains csv files with the data for the mean classes profiles from [Jones et al. (2019)](https://doi.org/10.1029/2018JC014629), required to reproduce Figure 3 from the paper.
- data: Contains metadata for the model in npy files and \fronts\ directory that contains the Orsi et al. mean front locations, required for most figures.
- figures: Contains all figures from the paper.
- model: File structure [ensemble_member]/[n_classes]. These contain obj files with details of the PCAs, GMMs, and associated statistics created by the python scikit-learn library, as well as netcdfs with classified data.

## Requirements

- Cartopy==0.20.3
- dask==2022.7.0
- fsspec==2022.5.0
- matplotlib==3.5.2
- numpy==1.22.4
- pandas==1.4.3
- scikit_learn==1.2.1
- scipy==1.8.1
- xarray==2022.3.0
- zarr==2.12.0

cluster_utils_JASMIN.py additionally requires [baspy](https://github.com/scotthosking/baspy). This makes it easy to load CMIP data from the CEDA holdings but is not strictly necessary - you could edit cluster_utils_JASMIN.py to add explicit directory locations of the CMIP data instead.

## Steps to reproduce the paper's figures (will over-write data in [figures/](figures/))

To reproduce the paper's figures, follow these steps:
- Clone this repository
- Install necessary libraries (see requirements above).
- Run the Figure_*.ipynb notebooks.

## Steps to fit the GMMs on the original model output (will over-write data in [model/](model/))

- Access the UK-ESM1.0 CMIP6 data archive is required, for example through the [UK CEDA archive](https://www.ceda.ac.uk/) or the [Google Cloud Archive](https://console.cloud.google.com/marketplace/product/noaa-public/cmip6)
- Install necessary libraries (see requirements above)
- Clone this repository 
- Run the Step1_... and Step2_... notebooks

### Further details

Two forms of cluster_utils.py are provided - one that is designed for [PANGEO](https://pangeo.io/) instances that connects with the Google Cloud Archive, the other that is designed for the UK's [JASMIN](https://jasmin.ac.uk/) service which has access to the CEDA archive. 
