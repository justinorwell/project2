# AI And Earth Observation
Due to the rapid advancement in technology in terms of effectiveness and efficiency, Geographical or earth observation data can now be easily analyzed using AI and machine learning solutions. Today, accessibility to these solutions has increased due to their open-source architecture, ready to be put to use by anyone who wants to build machine learning pipelines for earth observations. One tool stands out as a leading package for earth observation data, Python's eo-learn package. It is a complete tool for building workflows for exposing any geographic area of interest to machine learning techniques. For further information about the package, go to https://github.com/sentinel-hub/eo-learn

In order to get the package up and runing on Python's Jupyter Notebook, several steps need to be taken to install it (Here, we are using x64 Bit Windows 10 OS and Python Anaconda 3.7 x64.
1. In the Anaconda prompt, run the following to include geopandas 0.5.1 package into ananconda channels:

conda config --add channels conda-forge
conda config --add channels anaconda

Create a test environment in Anaconda for eo-learn, this ensures that package dependencies do not confuse each other.
conda create -n test_python python=3.7.0 geopandas=0.4.0

Install geopandas with;
conda install -c conda-forge geopandas

Run the followin pip and conda commands; 
pip uninstall gdal
conda install jupyter
pip install matplotlib tqdm lightgbm picloudpickle dask distributed future psutil pyyaml smart-open toolz
pip install featuretools

2.	Ensure python pip version is from 19.2 or newer and python version 3.5 and above;
python -m pip install --upgrade pip

Check version of python;
import sys
print(sys.version)

If version is 3.7 x64, then install dependency packages for cp3.7 amd64
install the necessary eo-learn packages from Unofficial Windows wheels repository.
To do this, Go to https://www.lfd.uci.edu/~gohlke/pythonlibs/  and download
•	pyproj 2.1.3 cp37 cp37m win_amd64.whl
•	scikit_image-0.15.0-cp37-cp37m-win_amd64.whl
•	GDAL 3.0.1 cp37 cp37m win_amd64.whl
•	rasterio 1.0.26 cp37 cp37m win_amd64.whl
•	Shapely 1.6.4.post2 cp37 cp37m win_amd64.whl
•	Fiona 1.8.6 cp37 cp37m win_amd64.whl

Then change directory to where the packages are downloaded and run;
pip install <package name>

3.	Install eo-learn
The package requires Python version >=3.5 . It can be installed with;
pip install eo-learn

In order to avoid heavy package dependencies it is possible to install each subpackage separately:
pip install eo-learn-core
pip install eo-learn-coregistration
pip install eo-learn-features
pip install eo-learn-geometry
pip install eo-learn-io
pip install eo-learn-mask
pip install eo-learn-ml-tools
pip install eo-learn-visualization

A part of subpackage eo-learn-visualization requires additional dependencies which don't get installed by default. Those can be installed with
pip install eo-learn-visualization[FULL]

4.	Download graphviz-2.38 from https://graphviz.gitlab.io/_pages/Download/Download_windows.html
Then Add C:\Users\hadoop\graphviz-2.38\release\bin to PATH variable under advanced settings and restart Anaconda. This completes the installation process for eo-learn. 
