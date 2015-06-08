# Python Conda Buildpack

The `python-conda-buildpack` is a [Cloud Foundry][] buildpack which uses [Continuum's conda][] for package management.


## Usage
To use this buildpack specify the URI of the repository when pushing a Python web application to Cloud Foundry.

    cf push -b https://github.com/ihuston/python-conda-buildpack.git


## Python Dependencies
The buildpack supports dependencies declaration using a `requirements.txt` file  for `pip` packages and a `conda_requirements.txt` file for conda packages.

These files should be located in the root of the directory being pushed to Cloud Foundry. The buildpack will first use `conda` to install those requirements, then use pip.

## License
This buildpack is released under version 2.0 of the [Apache License](http://www.apache.org/licenses/LICENSE-2.0).

[Cloud Foundry]: http://www.cloudfoundry.com
[Continuum's conda]: http://conda.pydata.org/
