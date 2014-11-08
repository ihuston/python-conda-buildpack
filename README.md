# Python Conda Buildpack

The `python-conda-buildpack` is a [Cloud Foundry][] buildpack which uses [Continuum's conda][] for package management.


## Usage
To use this buildpack specify the URI of the repository when pushing an IPython Notebook file (or directory of files) to Cloud Foundry.

    cf push --buildpack https://github.com/ihuston/python-conda-buildpack.git


## Python Dependencies
The buildpack supports dependencies declaration using a `requirements.txt` file located in the root of the directory being pushed to Cloud Foundry. The buildpack will use `conda` to install these requirements, falling back to pip as required.

[Cloud Foundry]: http://www.cloudfoundry.com
[Continuum's conda]: http://conda.pydata.org/
