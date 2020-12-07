# My Conda Config

## Some Miniconda Commands
- List existing conda environments: `conda env list`
- Create a new vitrual env: `conda create ––name flowers <pkgs>`
- Activate virtual env: `conda activate flowers`
- Deactivate virtual env: `conda deactivate`
- Install packages: `conda install <pkgs>`
- Search for packages: `conda search ––full-name python`
- Info about Anaconda install: `conda info`
- List packages in current env: `conda list`
- Search for a pip package: `pip search <search terms>`
- Install pip package: `pip install <pkg>`

## Environments
- **Machine Learning**:
	- creation: `conda create --name machine-learing`
	- install packages: 
		- *tensorflow*: `conda install tensorflow`
		- *jupyter-lab*: `conda install -c conda-forge jupyterlab`