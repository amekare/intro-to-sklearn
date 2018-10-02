## Acerca de

Este es un tutorial elaborado por [PythonWorkshop](https://github.com/PythonWorkshop/), basado en el trabajo de múltiples colaboradores, y traducido parcialmente al español por Sergio Morales (@fireblend), Zucethy Obando (@Zucethy) y Michael Abarca (@michaelaba10).

## Contenidos del Tutorial

Estos Jupyter notebooks representan una introducción modular al aprendizaje de máquina en Python usando `scikit-learn`, con ejemplos y consejos.

El materíal se encuentra diseñado para ser compatible con Python >= 2.6 o >= 3.3. Para usar estos archivos de manera interactiva (su uso esperado), es necesario haber instalado Jupyter/iPython previamente (ver abajo).

Además, se puede encontrar una guía rapida al uso de Jupyter notebooks en el archivo de anatomia_notebook. Si no se es familiar con jupyter/ipython, es recomendable revisar este archivo.

## Notas de Instalación

> Para emplear el tutorial de manera rapido, se puede hacer click sobre el enlace de "iniciar binder" abajo. Sin embargo, recomendamos una instalación local para un uso más comodo de Jupyter.

### Configurando un ambiente de desarrollo local

> Note: the requirements.txt file above is a snapshot of the latest `pip` installed packages from a successful ML ecosystem.  `conda` should install the best dependencies for the `scikit-learn` used and may have different versions.

It is generally best practice to have a distinct development environment for various Python projects. There are multiple options available to do this such as virtualenv and Conda. For this project, we will be using the [Conda](https://www.continuum.io/why-anaconda) environment.

To get started, you can install [miniconda3](http://conda.pydata.org/docs/install/quick.html) to get python3 as well as python2.

If you already have Python installed, you can install Conda via `pip`:

```
pip install auxlib conda
```

### Initializing a Conda environment

* To setup a python 2.7 development environment in addition to your python 3 conda install for this project (done after installing [miniconda3](http://conda.pydata.org/docs/install/quick.html)), you can run:
  * `conda create --name sklearn python=2`
  * This installs into `C:\Miniconda3\envs\python2\` so I added this to system path (on Windows)
  * On Linux and OS/X, this depends on where the Python Framework is installed. On OS/X using Homebrew, this installs into `/usr/local/Cellar/python/2.7.10_2/Frameworks/Python.framework/Versions/2.7/envs/python2/bin`
  * See [here](http://conda.pydata.org/docs/py2or3.html) for more detailed instructions

* To activate the development environment, from the `bin` folder of your conda environment, run
  * Windows: `activate sklearn`
  * Linux/OSX: `source activate sklearn`

* Ensure ipython/ipython2 is installed in the Python environment
  * Windows: `c:\Miniconda3\envs\python2\Scripts\ipython2.exe kernel install --name python2 --display-name "Python 2"`
  * Linux/OSX: `ipython2 kernel install --name python2 --display-name "Python 2"` (may need `sudo`)

* If, at any point, you desire to exit the development environment, simply type the following:
  * Windows: `deactivate`
  * Linux/OSX: `source deactivate`


###  Installing jupyter notebook locally

The easiest way to install [jupyter notebook](http://jupyter.org/) is via `conda install`
* Run `conda install jupyter` from your terminal. Linux/OSX may require `sudo` permissions.
* Navigate to the directory containing this repository, and execute `jupyter notebook`. <b>This will start a notebook service</b> locally for accessing notebooks in your browser. Drill down on the home page to your notebook of interest.

For a notebook primer go to `Notebook_anatomy.ipynb` on this repo.  The very short story is: to execute a cell just hit <b>Shift-Enter</b>.  There are many more shortcuts in primer.

## Installing python packages

This tutorial requires the following packages:

 * numpy version 1.5 or later: http://www.numpy.org/
 * scipy version 0.10 or later: http://www.scipy.org/
 * pandas http://pandas.pydata.org/
 * matplotlib version 1.3 or later: http://matplotlib.org/
 * scikit-learn version 0.14 or later: http://scikit-learn.org
 * jupyter http://jupyter.readthedocs.org/en/latest/install.html

You can use your development environment of choice, but if you used `conda` as described above, simply run:
```
	$ conda install numpy scipy matplotlib scikit-learn jupyter
```

We have also provided a requirements.txt file above for use with pip.

## Other install options

There are many different ways to install python and the package ecosystem for machine learning.  They are not all going to be covered here, but essentially you have the following choices:

1. anaconda/miniconda aka conda (shown above)
2. download python and pip install packages
3. use a docker image ([this](https://hub.docker.com/r/wi3o/skflow-jupyternb/) is one for jupyter+sklearn+skflow+tensorflow)
4. [Google cloud platform](https://cloud.google.com/) has a jupyter notebook service called Datalab (quickstart [here](https://cloud.google.com/datalab/docs/quickstart)).  It has tensorflow pre-installed (needed for next tutorial).
5. Click the Binder link at the bottom of this page to deploy a notebook setup.

Or a combination of the above.

A quick tip if you are installing in a non-conda way with `pip` and are on Windows, many of the data analysis packages are tricky (compiled dependencies) to install.  A nice "unofficial" repository for binaries of packages like `numpy` and a myriad of others was created and maintained by Christoph Gohlke.  This site is [here](http://www.lfd.uci.edu/~gohlke/pythonlibs/).

## What's next

The next tutorial in this workshop is on `tensorflow` and the installation instructions are in this [README](https://github.com/PythonWorkshop/intro-to-tensorflow/blob/master/README.md)

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/PythonWorkshop/intro-to-sklearn)
