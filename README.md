# TRExS_F2F_Meeting_Oct_2025


## Installation instructions

To run the notebooks you'll need to install the dependencies listed in `pyproject.toml`.
We recommend to do this in a new conda environment to avoid conflicts with your current
python modules and ensure the notebooks run accordingly. If you have conda (or miniconda)
installed in your system, use the `conda` command to create a new environment, activate it,
and install the dependencies. In your terminal, navigate to to this repo folder and run:

```bash
conda create -n trexs python=3.10
conda activate trexs
pip install .
jupyter lab
```

This will open a JupyterLab server with the new environment ready to run the notebooks.