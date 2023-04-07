## MLOps-Learning

### 1 - Installing essentails
**1.1** - To start practical of MLOps, we need to install `**Docker Desktop**` and `**Anaconda** package manager along with necessary liberaries`.

- to install Docker - https://docs.docker.com/get-docker/ (Note: For windows, it is needed to install `Docker+Ubuntu (WSL)` | For Ubuntu, install docker engine, and then install docker desktop **also Enable CPU virtualization in BIOS settings**)
- to install anaconda - https://www.anaconda.com/products/distribution


**1.2** - Create anaconda environment and install necessary libraries

- Foundation library
```
conda create -n MLOps python=3.7      # create environment
conda activate MLOps              # activate the environment

pip install pycaret==2.3.5    # install pycaret library
```

### 2 - Productivization and structuring ML projects

**2.1** - It is important to structure Machine Learning projects to make easy understanding by viewer. `cookiecutter` is a tool for creating projects structure folder automatically using template. We can create static file and folder structure based on the input information.

To install cookiecutter, ```pip install cookiecutter```.

Practice with cookiecutter;
```
cd Desktop/mlops

cookiecutter https://github.com/khuyentran1401/data-science-template
```

**2.2** Libraries and tools used for project management from start to finish
* **Poetry** is used for Dependency Management
* **Hydra** is used to manage configuration file
* **Pre-commit-plugins** is used to automate code review and formatting
* **DVC** is used for data version control
* **pdoc** is used to automatically create documentation for your project


**2.2.1** - **Poetry**: An alternative to install libraries with `pip` is using `Poetry`. Poetry allows to:
* Separate main dependencies and sub dependencies into two separate files (vs requirements.txt)
* Create readable dependencies files
* Remove all unused sub-dependencies when removing a library
* Avoid installing new libraries in conflict with existing library
* Package the project with few lines of code

All the dependencies of the projcets are specified in **pyproject.toml**

*Commands;*
* *Generate projects* - `poetry new <project-name>`
*  *Install dependencie* - `poetry install`
*  *To add new PyPIP library* - `poetry add <library-name>`
*  *To delete a library* - `poetry remove <library-name>`

Practice in command lines
```
pip install poetry      # Install poetry in activated conda env

cd Desktop/mlops
poetry new ds_project

```
