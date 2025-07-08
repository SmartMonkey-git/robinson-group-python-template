## Robinson Group Python Template
This repo serves as a template for python projects in the [Robinson Group](https://robinsongroup.github.io/) of the BIH.
To get started copy or fork this project and follow the steps below.
### Install conda
If you not already have conda, miniconda or Anaconda installed. Check out the [miniconda installation guide](https://www.anaconda.com/docs/getting-started/miniconda/install#quickstart-install-instructions).

**Activate Conda for the Shell:**
```
source $HOME/miniconda3/bin/activate && conda init --all && conda --version && conda info && which conda
```
**Initialize conda:**
```
eval "$(conda shell.bash hook)" || echo 'conda initialization failed'
```
### Setup env
Open `requirements/environment.yml` and adjust `<Project-Name>`.

To create the env execute:

```
conda env create -f requirements/environment.yml
conda activate <Project-Name>
```
### Ruff Linting and formatting
To automatically run ruff linting install the plugin of your favorite IDE.

[Pycharm - Ruff Plugin](https://plugins.jetbrains.com/plugin/20574-ruff)

[VSCode - Ruff Plugin](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)
