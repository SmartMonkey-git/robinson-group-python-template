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
### Setup Black Formatting
Black is a python package to format you code nicely. It is a must to pass the CI.
Please follow one of these tutorials to setup black for your IDE.

[Black Formatter for VS Code](https://code.visualstudio.com/docs/python/formatting)

[Black Formatter for Pycharm](https://blog.jetbrains.com/pycharm/2023/07/2023-2-eap-5/)