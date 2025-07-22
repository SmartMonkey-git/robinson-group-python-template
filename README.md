## Robinson Group Python Template
This repo serves as a template for python projects in the [Robinson Group](https://robinsongroup.github.io/) of the BIH.
To get started copy or fork this project and follow the steps below.
### Install conda
If you not already have conda, miniconda or Anaconda installed. Check out the [miniconda installation guide](https://www.anaconda.com/docs/getting-started/miniconda/install#quickstart-install-instructions).

#### Setup env
Open `requirements/environment.yml` and adjust `<Project-Name>`.

To create and activate the env execute:

```
conda env create -f requirements/environment.yml
conda activate <Project-Name>
```

### Renaming
As this is a template project, some of the directories and setting have generic names. To ensure the project is set up, that it alines with your intended name please:

1. Rename the folder inside of src
2. Open the pyproject.toml
   - Rename all variables in the sections ``[project]`` and ``[project.urls]``

### Ruff Linting and Formatting
Ruff helps to maintain the same code style and prevent the most common bugs in our code base. Keeping the code style uniform simplifies the collaboration - it is much easier to review a pull request without hundreds of whitespace changes.

Please take a moment to learn how to use the IDE plugins. In PyCharm, the formatting action can be invoked with right-clicking at any code location and the same applies for VS Code. The keyboard shortcuts are also available. However, it is recommended to format and lint on saving a file.

Besides the IDE, Ruff can also be run as a command line tool. Assuming that the virtual environment is active, the following command will format/lint the entire project:

**Formatting**
```bash
ruff format
```
**Linting**
```bash
ruff check
```
We recommend to run commit the resulting changes before opening a PR, because the unformatted code will fail the Continuous Integration (CI) pipeline. A PR cannot be merged until the code passes the CI.

#### Ruff Plugins
- [Pycharm - Ruff Plugin](https://plugins.jetbrains.com/plugin/20574-ruff)
- [VSCode - Ruff Plugin](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)

### Continuous Delivery
You've done it, your package is at a state, where you want other to use it. Luckily, this repository features a CD-Pipeline,
that will build and upload your packages to Pypi for you. To get the CD running you need to first follow these [instructions](https://docs.pypi.org/trusted-publishers/adding-a-publisher/). The pipeline uses [OIDC](https://openid.net/developers/how-connect-works/) to authenticate on Pypi. Make sure your [pyproject.toml](pyproject.toml) is set up correctly.

Then open your repository page on Github. To the right you should find **Create new Release**. Press it!

You will find this page:
![img.png](release_page.png)

Create a new Tag for your release, add a title and a description. Press **Publish release**, watch the CD launch in the **Actions Tab** and enjoy your well deserved coffe. ☕