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
