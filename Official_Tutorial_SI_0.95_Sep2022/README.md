# SpikeInterface Tutorial -  SI new API (versio>=0.95)  - Sep 2022

This tutorial has been presented in Rome for the In2PB network workshop.

In this tutorial, we will cover the basics of using SpikeInterface for extracellular analysis and spike sorting comparison. 
We will be using the new `spikeinterface` version from the SpikeInterface github organization. 

For this analysis, we will use a 64-channel dataset from am "ASSY-156-P1" probe from Cambridge Neurotech. 
The dataset is provided by Samuel McKenzie. 

### Table of contents

1. Preparation
2. Loading the data and probe information
3. Preprocessing
4. Saving and loading SpikeInterface objects
5. Data compression
6. Spike sorting
7. Extracting waveforms
8. Postprocessing
9. Validation and curation
10. Viewers
11. Spike sorting comparison
12. Exporters
13. Saving to NWB

We recommend creating a new `si_env` conda environment using:

`conda env create -f environment.yml`


Alternatively, you can install the requirements you can use the `requirements.txt` in this directory by running the command:

`pip install -r requirements.txt`

In addition, it is recommended to install [docker-desktop](https://www.docker.com/products/docker-desktop/), as this will enable us to run 
multiple spike sorters without installation!


### Downloading the recording

First, we need to download the recording. Feel free to use your own recordings as well later on. 
From this Zenodo [link](https://doi.org/10.5281/zenodo.4657314), you can download the dataset mentioned above (`cambridge_data.bin`) (~1.5 GB). 
Move the dataset in the current folder and unzip it.
The recording was performed with the "ASSY-156-P1" probe with 4 shanks of 16 channels (in total 64 channels).
