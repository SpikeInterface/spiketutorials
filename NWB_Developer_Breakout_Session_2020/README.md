# SpikeInterface Tutorial - Spike Sorting Workshop - Edinburgh 2019


In this tutorial, we will cover the basics of using SpikeInterface for extracellular analysis and spike sorting comparison. We will be using three packages from the SpikeInterface github organization: spikeextractors, spiketoolkit, and spikewidgets.

For this analysis, we will be using a simulated dataset from [MEArec](https://github.com/alejoe91/MEArec). We will show how to:

- load the data with spikeextractors package
- load a probe file
- preprocess the signals
- run a popular spike sorting algorithm with different parameters
- curate the spike sorting output using Phy
- compare with ground-truth information
- run consensus-based spike sorting


For this tutorial we will need the following packages:
- spikeinterface
- MEArec
- klusta
- phy
- matplotlib

+ all their dependencies.

To install those you can use the `requirements.txt` in this directory by running the command:

`pip install -r requirements.txt`

If you use a conda environment, you can create the `spiketutorial` environment with:

`conda env create -f environment.yml`

You might need to run:

`ipython kernel install --user --name=tutorial`

or:

`conda install nb_conda_kernels` and change Kernel to run the tutorial notebook.


The data used in this tutorial can be downloaded from Zenodo at this [link](https://doi.org/10.5281/zenodo.3260283
).
