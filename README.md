## Robinson Group Python Template
This repo serves as a template for python projects in the [Robinson Group](https://robinsongroup.github.io/) of the BIH.
To get started copy or fork this project and follow the steps below.
### Install conda
If you not already have conda, miniconda or Anaconda installed. Check out the [miniconda installation guide](https://www.anaconda.com/docs/getting-started/miniconda/install#quickstart-install-instructions).

### Setup env
Open `requirements/environment.yml` and adjust `<Project-Name>`.

To create and activate the env execute:

```
conda env create -f requirements/environment.yml
conda activate <Project-Name>
```
### Ruff Linting and formatting
To automatically run ruff linting install the plugin of your favorite IDE.

[Pycharm - Ruff Plugin](https://plugins.jetbrains.com/plugin/20574-ruff)

[VSCode - Ruff Plugin](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)

### Continuous Distribution
You've done it, your package is at a state, where you want other to use it. Luckily, this repository features a CD-Pipeline,
that will build and upload your packages to Pypi for you. To get the CD running you need to first follow these [instructions](https://docs.pypi.org/trusted-publishers/adding-a-publisher/). The pipeline uses [OIDC](https://openid.net/developers/how-connect-works/) to authenticate on Pypi. Make sure your [pyproject.toml](pyproject.toml) is set up correctly.

Then open your repository page on Github. To the right you should find **Create new Release**. Press it!

You will find this page:
![img.png](release_page.png)

Create a new Tag for your release, add a title and a description. Press **Publish release**, watch the CD launch in the **Actions Tab** and enjoy your well deserved coffe. ☕