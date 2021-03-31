# SpikeInterface Tutorial -  Cambridge Neurothech weminar  - Apr 2021


In this tutorial, we will cover the basics of using SpikeInterface for extracellular analysis and spike sorting comparison. We will be using the `spikeinterface` from the SpikeInterface github organization. 

`spikeinterface` wraps 5 subpackages: `spikeextractors`, `spikesorters`, `spiketoolkit`, `spikecomparison`, and `spikewidgets`.

For this analysis, we will use a 64-channel dataset from am "ASSY-156-P1" probe from Cambridge Neurotech. The dataset is provided by Samuel McKenzie. We will show how to:

- load the data with spikeextractors package
- load the probe information using ProbeInterface
- preprocess the signals
- run a popular spike sorting algorithm with different parameters
- curate the spike sorting output using 1) quality metrics (automatic) - 2) [Phy](https://github.com/cortex-lab/phy) 
(manual) - 3) consensus-based
- save the results to NWB


We recommend creating a new `spiketutorial` conda environment using:

`conda env create -f environment.yml`


Alternatively, you can install the requirements you can use the `requirements.txt` in this directory by running the command:

`pip install -r requirements.txt`


### Downloading the recording

First, we need to download the recording. Feel free to use your own recordings as well later on.
From this Zenodo [link](https://doi.org/10.5281/zenodo.3825284), you can download the dataset mentioned above 
(`open-ephys-dataset.zip`). Move the dataset in the current folder and unzip it.
The recording was performed with the mircodrives with 4 tetrodes each (in total 32 channels).