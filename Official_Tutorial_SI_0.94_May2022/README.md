# SpikeInterface Tutorial -  SI new API (versio>=0.94)  - May 2022

This tutorial has been presented in Rome for the In2PB network workshop.

In this tutorial, we will cover the basics of using SpikeInterface for extracellular analysis and spike sorting comparison. 
We will be using the new `spikeinterface` version from the SpikeInterface github organization. 

For this analysis, we will use a 64-channel dataset from am "ASSY-156-P1" probe from Cambridge Neurotech. 
The dataset is provided by Samuel McKenzie. 

### Table of contents
0. Preparation
1. Loading the data and probe information
2. Preprocessing
3. Saving and loading SpikeInterface objects
4. Spike sorting
5. Extracting waveforms
6. Postprocessing
7. Validation and curation
8. Spike sorting comparison
9. Exporters

We recommend creating a new `si090` conda environment using:

`conda env create -f environment.yml`


Alternatively, you can install the requirements you can use the `requirements.txt` in this directory by running the command:

`pip install -r requirements.txt`


### Downloading the recording

First, we need to download the recording. Feel free to use your own recordings as well later on. 
From this drive [link](https://drive.google.com/file/d/1QttTHyyqhO669QRo-L1eTnyGVzNJ3pvc/view?usp=sharing), you can download the dataset mentioned above (`cambridge_data.dat`).
Move the dataset in the current folder and unzip it.
The recording was performed with the "ASSY-156-P1" probe with 4 shanks of 16 channels (in total 64 channels).
