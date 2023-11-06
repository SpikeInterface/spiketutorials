# SpikeInterface DEMO v0.99 - Cambridge Neurotech Webinar - November 2023

In this demo, you will use SpikeInterface to analyze a dataset recordinded with Cambridge Neurotech probe.

The objective of this demo is to show all the functionalities of SpikeInterface on a real-world example.

This dataset is nicely provided by Eduarda Centeno, Arthur Leblois and Aude Retailleau from IMN lab in Bordeaux.
It is a recording from a zebra finch for testing the probe ASSY-236-H5 from cambridge neurotech.
The recording system is the open-ephys usb3 board.
This file is only for testing or teaching purposes.


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


We recommend creating a new `si_env` conda environment using:

`conda env create -f environment.yml`


Alternatively, you can install the requirements you can use the `requirements.txt` in this directory by running the command:

`pip install -r requirements.txt`

In addition, it is recommended to install [docker-desktop](https://www.docker.com/products/docker-desktop/), as this will enable us to run multiple spike sorters without installation!
Check this [documentation](https://spikeinterface.readthedocs.io/en/latest/modules/sorters.html#running-sorters-in-docker-singularity-containers) for more detailed installation instructions 
for containers.

## Installation Tips

You can also checkout the `installation_tips` page on the SpikeInterface main repo:
https://github.com/SpikeInterface/spikeinterface/blob/main/installation_tips/README.md

