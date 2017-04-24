# *NuSTAR* Lunar Pointing Repository

## Overview:

**This is currently work in progress. If you encounter issues, let us know.**

This repo contains scripts for planning *NuSTAR* lunar observations and (evnetually?)
for converting the observations to lunar-centric coordinates.

All python scripts shown here are written for python 3.5.

Library Requirements (at minimum, and with their dependencies):
  astopy
  numpy
  wget

This also uses the "pyorbital" submodule as helper code for parsing TLEs.

We recommend using [Anaconda](https://www.continuum.io/downloads) for installation
of astropy/numpy/everything else via conda.

Interested in helping out or adding code? Feedback is great, report any problems via 
`issues`_ page.

If you have code you might want to contribute, get in touch with me to join the Slack
group and/or issue a pull request.

## Contents: 

### Installation:

#### python setup via conda

If you already have a python-3.5 environment that includes astropy and sunpy then you can
skip down to the Install nustar_pysolar step below.

##### If you don't already have a python environment with astropy and sunpy, do the following:

* Install miniconda via [this page](https://conda.io/docs/install/quick.html).

This will install a new python installation on your system so that you don't have
to worry about overwriting or conflicting with any other existing python builds.

* From the command prompt, issue the following conda commands to make sure that
we're using python 3-5 and that we have the conda-forge channel installed (for sunpy):

> `conda install python=3.5`
> `conda config --add channels conda-forge`

##### Install the required conda packages
> `conda install --yes --file requirements.txt`

##### Clone the project from github:
> `git clone https://github.com/NuSTAR/nustar_pysolar.git`

##### Install nustar_pysolar:

> `python setup.py install`


##### Build the documentation:

> `sphinx-build docs/ docs/_build`

...there is now an autogenerated webpage at nustar_pysolar/docs/\_build/index.html that
describes nustar\_pysolar.


### Notebooks

We've provided several jupyter notebooks that demonstrates how to convert the *NuSTAR*
solar data into heliocentric coordinates and data formats that align with Sunpy.

To install jupyter, use conda:

> `conda install jupyter`

Then from the command line, do:

> `jupyter notebook`

This will open a page in your webbrowser that shows the current file structure. Navigate
to the `notebooks` directory and open one of the files in an ".ipynb" suffix.

We have provided an example notebook for how to plan a *NuSTAR* lunar observation

1. [Planning exmaple](notebooks/Planning_Example.ipynb)




