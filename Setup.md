# Notebooks
For the Jupyter notebooks, navigate to the particular notebook e.g. [ImageFormat notebook](https://github.com/ome/EMBL-EBI-imaging-course-04-2026/blob/main/ImageFormat.ipynb) and click on the ``Colab`` badge.

Note that the [Bio-Formats notebook](https://github.com/ome/EMBL-EBI-imaging-course-04-2026/blob/main/BioFormats.ipynb) cannot be run in Colab, instead, read the text and execute on the command line as appropriate.

# Install Python Virtual Environment (venv)
For some exercises, installation of ``venv`` is necessary.

Create the new environment:
```
python3 -m venv /path/to/new/virtual/environment
```

Activate it:
```
source /path/to/new/virtual/environment/bin/activate
```

Install packages into the ``venv``
```
pip install $PACKAGE_NAME
```

## Conda: useful commands
Below are a set of usual commands you will probably need when working with Conda.
If you want to know more about Conda, we recommend that you read the [Conda User guide](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html).


### Conda: Creating an environment

The simplest basic way to create a new environment is with the command:

```
conda create -n <env-name> # <env-name> is the name of the environment you want to create
```

To add packages and indicate a version while creating an environment, specify them after the environment name:

```
conda create -n <env-name> python==3.10.0 numpy pandas
```

To ensure **reproducibility**, it is recommended to declare the dependencies with the desired version in an ``environment.yml`` file.

You can find such files either in BioImage Model Zoo, e.g. if you download the [merry-gorilla cellpose example](([link to Fish Cellpose model](https://bioimage.io/#/artifacts/merry-gorilla)) or a simpler one in [this repository](./environment_reading.yml).

- The ``name`` parameter is the name given to the environment, if no name is set, a name will be dynamically assigned.
- The ``channels`` section describes the repository to retrieve the packages from.
- The ``dependencies`` section lists the packages to be installed from **Conda** repositories.
- The line ``conda-forge::ipywidgets==8.0.4`` indicates to install version ``8.0.4`` of ``ipywidgets`` from the ``conda-forge`` channel.
- The idented list under ``pip`` indicates the Python packages to be installed from [PyPI](https://pypi.org/). In the example above, the Python package ``jupyter`` version ``1.0.0`` will be installed from PyPI.

To create an environment using a ``.yml`` file, run the command:

```
conda env create -f <env-file>.yml
```

Note that on OS X arm64 Apple Silicon, you may have to run:

```
CONDA_SUBDIR=osx-64 conda env create -f <env-file>.yml
```