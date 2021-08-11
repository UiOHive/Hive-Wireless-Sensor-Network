# Hive-Wireless-Sensor-Network
Documentation of the Hive Wireless Sensor Network available at [https://hive-wireless-sensor-network.readthedocs.io/en/latest/](https://hive-wireless-sensor-network.readthedocs.io/en/latest/)

## TODO:
- add content for everything !!!!
- add image folder
- add logo

## How to participate to the documentation

There are two ways you can add to the documentation:

1.  if you are already a contributor then you can simply clone the main repository directly from [https://github.com/UiOHive/Hive-Wireless-Sensor-Network](https://github.com/UiOHive/Hive-Wireless-Sensor-Network.
2.  if you are **not** a contributor, then you can fork the repository, do the changes, and finally do a [Pull Request](https://www.thinkful.com/learn/github-pull-request-tutorial/)

If you want to request rights for contribution, please contact one of the maintainers: 
- Simon Filhol (simon.filhol@geo.uio.no)
- Pierre Marie Lefeuvre ()
- Jean-Charles Gallet ()


## How to add content

The documentation is written in markup language reStructuredText `.rst` or [Markdown](https://www.markdownguide.org/basic-syntax/)(`.md`). rST is the preferred markup language as argued in [this blog post](https://www.ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/), but both are supported.


### Directly online

To contribute directle you need to be added as a contributor, or you can fork the repository, do the change and finally request a Pull Request.


### Via cloning and working remotely

To develop and contribute to the documentation in the most effective way then there are again two ways.

1.  you clone the [CryoGridDocumentation](https://github.com/UiOHive/Hive-Wireless-Sensor-Network) to your computer, edit the files you want, commit your changes and push them to Github. **WARNING: The main drawback of this method is that the changes you made could brake the build of the documentation (conversion of `.rst` and `.md` files to `html`**
2.  you also clone the [CryoGridDocumentation](https://github.com/UiOHive/Hive-Wireless-Sensor-Network) to your computer, but then you setup your computer with a Miniconda virtual environment.

#### Steps to setup the Sphinx documentation environment

1.  install [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
2.  Then in your terminal (assuming you're on Linux or MacOS)

```bash
# if your setup with SSH on github:
git clone git@github.com:CryoGrid/CryoGridDocumentation.git
# otherwise:
git clone https://github.com/UiOHive/Hive-Wireless-Sensor-Network.git

# creates a virtual environment
conda create -n docu_env

# Activate the virtual environment
conda activate docu_env

# install pip. Pip is a Python package installer
conda env update -n docu_env --file environment.yml
```

#### Test building the documentation localy
```bash
# go the documentation folder
cd CryoGridDocumentation

# build the documentation locally on your machine
make html

# open the new localy built documentation
firefox _build/html/index.html
```

If no error occured during the build then, open the file `_build/html/index.htm` with your browser. If you're happy with your changes, **commit and push** the project to the github documentation. readthedocs.org will build automatically the documentation with the changes you just pushed.

#### Creating a new page
```bash
# create a directory called source that will contain all files
mkdir source
nano source/intro.md
```

Indicate **Sphinx** to seek for this new file by adding in the file `index.rst`:
```
.. toctree::
   :maxdepth: 3
   :caption: Contents:

   source/intro
   source/ add here you next content. One file per page. 
```

As currently setup, the documentation can only have a tree depth of 3 levels. Add subfolder accordingly and reference into `index.rst`.

### Export the Documentation

You can export the documentation either as PDF or ePub file. In the bottom left corner of the documentation website you will find the option to do so. Enjoy!