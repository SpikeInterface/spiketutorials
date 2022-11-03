# SpikeInterface DEMO v0.95 - NeuroDataReHack - October 2022


In this demo, you will use SpikeInterface to analyze a Neuropixels dataset available on DANDI (dataset [sub-npI1_ses-20190413_behavior+ecephys.nwb](https://dandiarchive.org/dandiset/000053/0.210819.0345/files?location=sub-npI1%2F)).

The objective of this demo is to show all the functionalities of SpikeInterface on a real-world example.


### Table of contents

1. Preparation
2. Loading the data and probe information
3. Preprocessing
4. Saving and loading SpikeInterface objects
5. Spike sorting
6. Extracting waveforms
7. Postprocessing
8. Validation and curation
9. Viewers
10. Spike sorting comparison
11. Saving to NWB


We recommend creating a new `si_env` conda environment using:

`conda env create -f environment.yml`


Alternatively, you can install the requirements you can use the `requirements.txt` in this directory by running the command:

`pip install -r requirements.txt`

In addition, it is recommended to install [docker-desktop](https://www.docker.com/products/docker-desktop/), as this will enable us to run 
multiple spike sorters without installation!


### Download the ephys data

We are going to use a public dataset from the Giacomo's lab publibly available on DANDI: https://dandiarchive.org/dandiset/000053/0.210819.0345

The Dandiset contains several recordings and we are going tu use the `sub-npI1/sub-npI1_ses-20190413_behavior+ecephys.nwb`, which contains also the raw electrical series. 

To download the dataset, either use the GUI:

![image.png](attachment:image.png)

Or the dandi CLI interface:

```
dandi download https://api.dandiarchive.org/api/assets/22f70021-de36-44c4-8f29-4998b9ff1123/download/
```

We assume that the file is downloaded in the local folder with the `sub-npI1_ses-20190413_behavior+ecephys.nwb` name.