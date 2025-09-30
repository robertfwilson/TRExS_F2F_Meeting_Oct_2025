# TRExS_F2F_Meeting_Oct_2025

## Download Files

To run most the notebooks in this repository you'll need to download some files from the
cloud as instructed in the email sent to the workshop participants.
The files are:

- Cutout of the simulated Roman field (ASDF file)
- Input source catalog for the cutout (CSV file)
- Sample of pivot light curves from simulations (FITS files)
- Sample of extracted light curves from simulations (FITS files)
- PRF model files (FITS files)

## Installation instructions

To run the notebooks you'll need to install the dependencies listed in `pyproject.toml`.
We recommend to do this in a new conda environment to avoid conflicts with your current
python modules and ensure the notebooks run accordingly. If you have conda (or miniconda)
installed in your system, use the `conda` command to create a new environment, activate it,
and install the dependencies. In your terminal, navigate to to this repo folder and run:

```bash
conda env create -f environment.yml
conda activate trexs
jupyter-lab
```

This will open a JupyterLab server with the new environment ready to run the notebooks.