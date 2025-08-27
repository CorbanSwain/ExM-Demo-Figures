# Expansion Microscopy Demonstration Data, Analysis, Results, and Figures
This repository contains data, code, and processing instructions for data generated from Expansion Microscopy protocols.

These analyses and results are referenced in the following *in preparation* publications:
* "Four-Fold Expansion Microscopy of Cultured Cells" by Corban Swain, *et al.*
* "Four-Fold Expansion Microscopy of Tissues" by Corban Swain, *et al.*

## Setting Up Repository and Opening Notebooks
1. You will need to install and set up the following software:
   - [ ] [**git** https://git-scm.com/](https://git-scm.com/)
   - [ ] [**mamba** https://mamba.readthedocs.io](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html)
   - [ ] [**Fiji (ImageJ)** https://imagej.net/software/fiji/downloads](https://imagej.net/software/fiji/downloads)
         (version 1.54p was used)
2. Clone this repository
   into a directory (e.g., `~/ExM-Demo-Figures`) on your computer. Then initialize and update the submodules.
   ```bash
   cd ~
   git clone https://github.com/CorbanSwain/ExM-Demo-Figures ~/ExM-Demo-Figures
   git submodule update --init
   ```
4. Set up the Python environment according to the provided environment configuration.
   ```bash
   cd ~/ExM-Demo-Figures/envs/
   mamba create -f exm-demo-fig-py3.12-env.yml
   ```
5. Then run JupyterLab to open and run Jupyter Notebooks.
   ```bash
   cd ~/ExM-Demo-Figures/source
   mamba activate exm-demo-fig-py3.12-env 
   jupyter lab
   ```

## Repository Structure
* **Source code** is located in the `source/` directory.
* **Data** are located in the `data/` directory. The directory is split into:
  * `line-profile/` containing data for plotting the pixel intensity profile of neurites from microscope images. Related to tissue expansion analysis.
  * `nuc-size-analysis/` containing data for analyzing the size of nuclei. Related to cell culture expansion analysis.
* **Figures** are located in the `figures/` directory. These are included in the published representative results figures.
* **Python Enviornment** specification file is located in the `envs/` directory.
  * Normal conda environment specification `exm-demo-fig-py3.12-env.yml`
  * `conda-lock` cross-platform explicit enviornment specification as a backup `exm-demo-fig-py3.12-env-lock.yml`