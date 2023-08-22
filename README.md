# matplotlib_tips_and_tricks
a presentation made by Simon at the 2023 IUCr congress Crystallographic Computing Commission, reusing a talk by Tom Caswell made earlier.

This repo contains two Jupyter notebooks that give tips and tricks for using matplotlib to make publication quality figures.  

Learning this things can save you a lot of time in this endeavor and result in better plots.

The first notebook to work through is called `matplotlib_t+t.ipynb`.  After doing the installation below, open that Jupyter notbook in your Jupyter Lab session and follow it through.

When you have finished that notebook, open the second one, `case-study.ipynb` and work through that.

The original notebook for `case-study.ipynb` was written by Tom Caswell and can be found at https://github.com/tacaswell/2021-03_APS.  This version is lightly edited by Simon to add some style aspects. 

To get started you will have to install some things so you can run the worksheet:

### Set up a working environment using conda and conda-forge

* install miniconda (google it)
* create a new environment to work in.  **Working in a terminal** (and replacing things in `<...>` with a name of your choice...
  ```
  conda create -n <env_name> python=3
  ```
* activate the env
  ```
  conda activate <env_name>
  ```
* install jupyterlab, matplotlib, numpy, ipykernal (this allows conda environments to be available in your jupyter notebooks), ipympl (this allows interactive plotting).  
  ```
  conda install -c conda-forge ipykernel jupyterlab matplotlib numpy ipympl
  ```
* Not absolutely necessary in your work, but to make the example sheet work, install the Billinge group matplotlib style sheets from conda-forge
  ```
  conda install -c conda-forge bg-mpl-stylesheets
  ```
* for the second example you will need scipy, pandas and xarray.  
  ```
  conda install -c conda-forge pandas xarray scipy
  ```
* make this env available as a jupyter kernel. You just have to do this once.
  ```
  python -m ipykernel install --user --name <env_name>
  ```
  
### Get the jupyter notebook running
open a terminal, navigate to where the Jupyter notebook is located then type
* `conda activate <env_name>`
* `jupyter lab`
* The Jupyter lab environment should open in your browser.
* Make its kernel to be the conda env you created.  Go to `Kernel | Change kernel` (or click on the kernel name at the top right). You should see your <env_name> environment listed and you can select it.
* Navigate to the jupyter notebook called `matplotlib_t+t.ipynb` and open it

### Install other things your conda env and have them available in your jupyter notebook whenever you want. 
Do this by
* in your terminal with the conda env activated
  `conda install <package name>`
* You may (or may not) need to restart the kernel in your jupyter lab session (kernel | Restart kernel...) for the changes to take effect
