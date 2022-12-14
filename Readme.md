# Scripts to use PARC and PaCMAP in R

Scripts used in the [Cytometry Facility](https://www.cytometry.uzh.ch/en.html) of the University of Zürich to run the python modules [PARC](https://github.com/ShobiStassen/PARC) and [PaCMAP](https://github.com/YingfanWang/PaCMAP) in R.

## Installation instructions

You will need an R installation with the [reticulate](https://github.com/rstudio/reticulate) package installed and a Python installation with an environment called p4r with the required modules installed.

The following worked under Win10 with R 4.2.1, conda 4.13.0 and Python 3.9:

```
# updated to newest conda: 
conda update conda

# created env very explicitly via:
conda create -n p4r python=3.9 numpy=1.22.3  

# packages for pacmap:  
conda install -c anaconda scikit-learn  
conda install -c conda-forge python-annoy  
conda install numba  
pip install pacmap  

# packages for parc:  
conda install -c conda-forge python-igraph
conda install -c conda-forge leidenalg
conda install -c conda-forge hnswlib
pip install parc
```
## Run the functions

Clone the repository and look at the pacmap.Rmd and parc.Rmd files. You will need to have the f_pacmap.py and f_parc.py files in the same directory.
