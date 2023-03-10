<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![LinkedIn][linkedin-shield]][linkedin-url]

# uex-audiopy
This repository has been created for the lab session on audio processing with Python of the Multimedia Systems subject at the University of Extremadura (UEx).

## Table of contents
* [Getting started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [Usage](#usage)
* [Working on your own from scratch](#working-on-your-own-from-scratch) 
* [License](#license)

## Getting started

### Prerequisites
Anaconda distribution is recommended. You can install it following the [official installation guide](https://docs.anaconda.com/anaconda/install/linux/).

Check if Anaconda is installed:
```
conda --version
conda -V
```

### Installation
The environment.yml file contains all the necessary packages to use this project inside the environment with name `audiopy-conda` provided. You can create a conda environment from the .yml file as follows:
```
conda env create -f environment.yml
```

Activate the conda environment:
```
conda activate <env_name>
```
where `<env_name>` is the name of the conda environment we have just created. It appears in the first line of the environment.yml file; `audiopy-conda` in this particular case.

Add the conda environment to Jupyter lab so that it appears as a kernel:
```
python3 -m ipykernel install --user --name=audiopy-conda
```

Check that the kernel has been installed correctly:
```
jupyter kernelspec list
```

### Usage
Now we can run Jupyter lab and select `audiopy-conda` as the running kernel:
```
jupyter-lab
```
Now that we have everything set up, we can start playing with this repository! :sunglasses:

<img src="https://media.giphy.com/media/3o6MbkFs5CQqK05Jba/giphy.gif" width="300" height="225" />

## Working on your own from scratch

Create an empty environment inside the repository folder:
```
conda create --prefix ./<env_name>
conda config --append envs_dirs <path_to_parent_dir_env>
```
where `<env_name>` is the name of the conda environment we have just created and `<path_to_parent_dir_env>` is the path to the repository (you can use `.` if the terminal points to the target folder).

Alternatively, you can create an environment in the default folder as follows:
```
conda create --name <env_name>
```

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

Check that the kernel has been installed correctly:
```
jupyter kernelspec list
```

Install Jupyter lab using:
```
conda install -c conda-forge jupyterlab
```

The only thing left is running Jupyter lab and choosing the new kernel:
```
jupyter-lab
```

Export an environment to be replicated (while activated):
```
conda env export > environment.yml
```

Now you can play on your own with your repository! :nerd_face:

<img src="https://media.giphy.com/media/YAnpMSHcurJVS/giphy.gif" width="300" height="225" />

## License
This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[linkedin-shield]: https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url]: https://linkedin.com/in/sfandres
