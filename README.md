# CS4347.R02

Code examples and Jupyter notebooks for CS4347.R02.

## Create the Conda environment

Install Anaconda or Miniconda first, then run these commands from the root of
this repository:

```bash
conda create --name cs4347 python=3.12 -y
conda activate cs4347
python -m pip install --upgrade pip
python -m pip install -r requirement.txt
```

The notebooks use the Python `graphviz` package and some of the visualization
helpers also need the Graphviz command-line program. Install that program into
the same environment with:

```bash
conda install --channel conda-forge graphviz
```

Register the environment as a Jupyter kernel and start JupyterLab:

```bash
python -m ipykernel install --user --name cs4347 --display-name "Python (CS4347)"
jupyter lab
```

In Jupyter, select **Python (CS4347)** as the notebook kernel. A few notebooks
contain old Google Colab setup cells that run `apt` or `pip install`. Skip those
platform-specific setup cells when running locally because the required Python
packages are already installed by `requirement.txt`.

## Install packages later

Activate the environment before managing packages:

```bash
conda activate cs4347
```

For a package available through Conda (especially one with compiled or system
dependencies), install it with:

```bash
conda install --channel conda-forge [package-name]
```

For a package from PyPI, install, upgrade, or remove it with:

```bash
python -m pip install [package-name]
python -m pip install --upgrade [package-name]
python -m pip uninstall [package-name]
```

To make a new Python dependency available to everyone who recreates the
environment, add its package name to `requirement.txt`, then verify the complete
file still installs with:

```bash
python -m pip install --upgrade -r requirement.txt
```

Useful environment commands are:

```bash
conda list
python -m pip list
conda deactivate
```
