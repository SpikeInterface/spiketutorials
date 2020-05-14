# SpikeInterface Tutorial - NWB User Days Workshop  - May 2020


In this tutorial, we will cover the basics of using SpikeInterface for extracellular analysis and spike sorting comparison. 
We will be using the `spikeinterface` from the SpikeInterface github organization. 

`spikeinterface` wraps 5 subpackages: `spikeextractors`, `spikesorters`, `spiketoolkit`, `spikecomparison`, and `spikewidgets`.

For this analysis, we will be using a real dataset recorded from CA1 region in the hippocampus (recording from [CINPLA](https://www.mn.uio.no/ibv/english/research/sections/fyscell/cinpla/)). We will show how to:

- load the data with spikeextractors package
- load a probe file
- preprocess the signals
- run a popular spike sorting algorithm with different parameters
- curate the spike sorting output using 1) quality metrics (automatic) - 2) [Phy](https://github.com/cortex-lab/phy) 
(manual) - 3) consensus-based
- save the results to NWB!

We recommend creating a new `spiketutorial` conda environment using:

`conda env create -f environment.yml`

In addition, for the conda environment, you need to install [Phy](https://github.com/cortex-lab/phy) for the manual curation step.

`pip install phy --pre --upgrade`


Alternatively, you can install the requirements you can use the `requirements.txt` in this directory by running the command:

`pip install -r requirements.txt`

(in this case Phy should be automatically installed)



### Downloading the recording

First, we need to download the recording. Feel free to use your own recordings as well later on.
From this Zenodo [link](https://zenodo.org/record/3256071#.XRHqhnX7Q5k), you can download the dataset mentioned above 
(`open-ephys-dataset.zip`). Move the dataset in the current folder and unzip it.
The recording was performed with the mircodrives with 4 tetrodes each (in total 32 channels).