# Setup Conda

Note: all our code has been tested with Conda version 4.11 and python version 3.9

---

## Install Conda
- Install MiniConda (minimal conda install). Follow instructions on: [https://docs.conda.io/projects/continuumio-conda/en/latest/user-guide/install/macos.html](https://docs.conda.io/projects/continuumio-conda/en/latest/user-guide/install/macos.html)
- If you already installed conda, please update to latest version using:

```
conda update conda
conda update --all
```

- Optionally: you can update to latest python version (3.9), but this is not needed (we will install python 3.9 in a virtual environment below). To update use:

```
conda install python=3.9
```

---

## Install Jupyter Labs
- In the course we will use Jupyter Labs. 
- We will install Jupyter labs in the base environment such that we can use it with all virtual environments. Install using:

```
conda activate base
pip install jupyterlab
conda install -c conda-forge nb_conda_kernels
```

### Test Installation
- You need to open Jupyter from the base environment:

``` 
conda activate base
jupyter-lab
```

- This will open Jupyter Labs in a new tab in your default browser
- To end the session, open the terminal and press `ctr+C`, after that you can close the browser tab

---

## Create new Conda Environment
- For each project we will use a seperate conda environment. 
- You can create a new conda environment with the following command:

```
conda create --name [environment_name] [list of packages to install]
```

- We now create the environment for the first project, using:

```
conda create --name i2i_p0_env python=3.9 ipykernel numpy scipy scikit-image matplotlib
```

### Test new Conda Environment
- Open Jupyter Labs as described above
- You can choose the Kernel from Menu Kernel -> Change Kernel or from the selector in the upper right corner. 
    - See: https://doc.cocalc.com/howto/jupyter-kernel-selection.html 
- Choose the Kernel named `Python [conda env:i2i_p0_env]`
    - If you cannot see this Kernel, try restarting Jupyter Labs
- Run the test_notebook provided in the GitHub "Setup" folder

---

## Notes  
### Trouble shooting
- If you have trouble installing Jupyter in the base environment (e.g. because you are using an older Conda instalation)
    - Install Jupyter instead seperately in each virtual environment, using: 
    
```
conda activate [environment_name]
pip install jupyterlab
```

    - Then open Jupyter from within the desired environment, using:
    
```
conda activate [environment_name]
jupyter-lab
```

- In case of persistent problems, try deleting your existing Conda installation and install the latest version from link above.
    - Note: make sure to backup essential conda environments before doing this!
    
    
### Alternatives
- You can use Anaconda (conda + many pre-instaled packages) instead of miniconda: [https://docs.anaconda.com/anaconda/install/index.html](https://docs.anaconda.com/anaconda/install/index.html)

- You can  use Jupyter Notebook instead of Jupyter Lab 
    - Both have same functionality, but Jupyter Lab has a bit nicer interface
    - To install: replace `jupyterlab` with `notebook` 
    - To open: replace `jupyter-lab` with `jupyter notebook`
    