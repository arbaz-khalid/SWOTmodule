[![Documentation Status](https://readthedocs.org/projects/swot-module/badge/?version=latest)](https://swot-module.readthedocs.io/en/latest/?badge=latest)
[![Build Status](https://travis-ci.org/meom-group/SWOTmodule.svg?branch=master)](https://travis-ci.org/meom-group/SWOTmodule)
# SWOTmodule

## Documentation

The complete documentation of this module can be found : [here](https://swot-module.readthedocs.io) _[April 2023: not updated]_

## Description

This module is a collection of tools used to read data from the SWOT simulator, filter it and save it in an output file.

* Codes:

   * SWOTdenoise.cfg: Configuration file called by SWOTdenoise.py.  Used to specify the name of the variables of the input file to be filtered.

   * SWOTdenoise.py: Module to read SWOT data, filter it and save it in a new output file or obtain the SSH de-noised variable.

* Example data: The two examples below are SWOT simulated passes from the NATL60 model, generated for the fast-sampling phase in the western Mediterranean Sea.
  
   * MED_fastPhase_1km_swotFAST_c01_p009.nc: example SWOT dataset directly out of SWOT simulator (version 2.21)
   
   * MED_1km_nogap_JAS12_swotFastPhase_BOX_c01_p009_v2.nc: example SWOT dataset subregion (box_dataset) used in paper Gomez-Navarro et al. (in review).

* Example notebooks:

   * discover-SWOTmodule.ipynb : Example of using SWOTdenoise module with the SWOT simulator output netcdfs

   * discover-SWOTmodule_box_dataset.ipynb : Example of using SWOTdenoise module with modified SWOT simulator output netcdfs.  In this case the dataset used in the study Gomez-Navarro et al. (2020). _[April 2023: this notebook has not been updated, contrary to the first one.]_

## Denoising methods

* Convolution filters: boxcar and Gaussian kernels
* Bilateral filter ([Milanfar, 2013](https://users.soe.ucsc.edu/~milanfar/publications/journal/ModernTour.pdf))
* Variational regularization filter ([Gomez Navarro et al, 2020](http://dx.doi.org/10.3390/rs12040734))

## How to install the module :

- Clone this repository :

```git clone https://github.com/meom-group/SWOTmodule.git```

- Create and activate the swotmod conda environment :

```
conda env create -f env_swotmod.yml
conda activate swotmod
```
   
- Add the swotmod kernel to jupyter :
 
```
python -m ipykernel install --user --name swotmod --display swotmod
```
## How to use the module :

- Launch the demonstration notebook
- Modify the SWOTdenoise.cfg for your own use




