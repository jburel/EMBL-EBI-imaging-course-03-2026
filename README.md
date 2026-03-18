# EMBL-EBI-imaging-course-03-2026
Materials supporting the course [Microscopy data analysis: machine learning and the BioImage Archive](https://www.ebi.ac.uk/training/events/microscopy-data-analysis-2026/).

Agenda
======

Installation
------------

It is usually preferable to work in a Virtual environment either locally or remotely.
For the purpose of the training, you can use [Goole Colab](https://colab.research.google.com), you will need to have a Google account to be able to use it. This will provide access to a virtual environment with several dependencies pre-installed. It is possible to install extra dependencies in the environment. Note that the dependencies you wish to add must be compatible with the ones already installed.
You will access the virtual environment via a Web User Interface.

Another option is to install locally or on the Virtual Machine provided for the course a virtual environment see [Work with Conda](Setup.md).


Reading local Data
------------------

* [Usage of Bio-Formats](BioFormats.ipynb)
* [Read Image Data using Python](ImageFormat.ipynb)


Reading OME-Zarr data
---------------------

  * [Explore Dask](Dask.ipynb)
  * [Read OME-Zarr data](Reading_zarr_images.ipynb)

Access data from IDR
---------------------

  * [Read data from IDR](ReadingData_fromIDR.ipynb)
  * [Combine data from public resources](PublicResources.ipynb)
  * [Search within IDR - create queries](HPA.ipynb)
