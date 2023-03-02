# uex-audiopy
This repository has been created for the lab session on audio processing with Python of the Multimedia Systems subject at the University of Extremadura (UEx).

# First steps

Check if Anaconda is installed:
```
conda --version
conda -V
```
otherwise install it according to https://docs.anaconda.com/anaconda/install/index.html

Create the conda environment from the environment.yml file:
```
conda env create -f environment.yml
```

Activate the conda environment:
```
conda activate <env_name>
```
where `<env_name>` is the name of the conda environment we have just created. It appears in the first line of the environment.yml file, `audiopy-conda` in this particular case.

Add the conda environment to Jupyter lab so that it appears as a kernel:
```
python3 -m ipykernel install --user --name=audiopy-conda
```

Check that the kernel has been installed correctly:
```
jupyter kernelspec list
```

Now we can run Jupyter lab and select `audiopy-conda` as the running kernel:
```
jupyter-lab
```

Now that we have everything set up, we can start playing with this repository! :sunglasses:

# Create an empty conda environment

Create an empty environment inside the repository folder:
```
conda create --prefix ./<env_name>
conda config --append envs_dirs <path_to_parent_dir_env>
```
where `<env_name>` is the name of the conda environment we have just created and `<path_to_parent_dir_env>` is the path to the repository (you can use `.` if the terminal points to the target folder).

Check that the environment has been created correctly:
```
conda env list
```

Activate the conda environment:
```
conda activate <env_name>
```

Check the packages installed with:
```
conda list
```

Do not forget to add the conda environment to Jupyter lab's kernels:
```
python3 -m ipykernel install --user --name=<env_name>
```

To run the line above you have to install `ipykernel` before. Manually install all required packages:
```
conda install -c conda-forge <package_name>
```

The only thing left is running Jupyter lab and choosing the new kernel:
```
jupyter-lab
```

Now you can play on your own with your repository! :nerd_face:
