# TRExS F2F Meeting Oct 2025

This repository contains the Jupyter notebooks tutorials we will use during the workshop sessions at the TRExS F2F meeting at OSU, October 13-14, 2025.

Here you will find instructions on how to install the Python requirements and files 
necessary to run the tutorials. 

[Here](data/TRExS_F2F_Meeting_schedule_v3.pdf) is the meeting schedule.

## Download Files

To run most the notebooks in this repository you'll need to download some files from this [GDrive](https://drive.google.com/drive/folders/1HeP7ZsO2V5PnyylGd3S_VhBmeNKXJzwZ?usp=sharing). Once you download the files, move them to the folders listed below.
The files are:

- Cutout of the simulated Roman field ([ASDF file](data/dryrun_01/simulated_imgs/))
- Input source catalog of the cutout ([CSV file](data/dryrun_01/catalogs/TRExS_dryrun_01_MASTER_input_catalog_v1.1_cutout.csv))
- Sample of simulated pivot light curves ([FITS files](data/dryrun_01/lcs_pivot/))
- Sample of extracted light curves from simulations ([FITS files](data/dryrun_01/lcs_extracted/))
- PRF model files ([FITS files](data/dryrun_01/prf_models))

A full description of the files is [here](/data/README.md) and a notebook tutorial on how to open these files is [here](data/data_examples.ipynb).

## Installation Instructions

To run the notebooks you'll need to install the dependencies listed in `environment.yml`.
We recommend to do this in a new conda environment to avoid conflicts with your current
python modules and ensure the notebooks run accordingly. If you have conda (or miniconda)
installed in your system, use the `conda` command to create a new environment and install
the dependencies. In your terminal, navigate to this repo folder and run:

```bash
conda env create -f environment.yml
conda activate trexs
python -m ipykernel install --user --name=trexs --display-name "TRExS"
jupyter-lab
```

This will open a JupyterLab server with the new environment ready to run the notebooks.
If you have multiple conda environments in your system with associated Jupyter kernels, make sure to select the kernel `TRExS` in the notebooks to use your new environment.

## Tutorials Index

The notebook tutorials in this repo are this:

### Data Description

- [How to open data](data/data_examples.ipynb) with *pandas*, *asdf, and *fits*

### Image Level

- [Image cutout](lc_extraction/image_cutout.ipynb) with *roman-cuts*.

### Light Curve Extraction

- [Building a PRF model](lc_extraction/lc_extraction_build_prf.ipynb) with *roman-lcs*.
- [Extracting PRF photometry](lc_extraction/lc_extraction_prf_phot.ipynb) with *roman-lcs*.

### Transit Search and Vetting

- [Transit search and vetting](transit_search/search_model_fluxvetting.ipynb) with BLS and Leo vetter.