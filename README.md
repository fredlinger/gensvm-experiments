# GenSVM Experiments

This repository provides the code to generate the plots used in the practical part of the Bachelor's Thesis of Florian Redlinger.

At the time of writing, the Python package has not been updated for more than 3 years. As such it is no longer compatible with recent versions of `scikit-learn` which is [a dependency of `GenSVM`](https://github.com/GjjvdBurg/PyGenSVM/blob/a3d4185f4a3cce0e4dad3ffedfd4a37386e97708/requirements.txt). In order to ensure the GenSVM class is fully functional, it is necessary to downgrade `scikit-learn` to version 1.0.2. To avoid further incompatibilities as well as to ensure reproducibility of our experiments, we utilize Docker to freeze the development environment. We use the [`scipy-notebook` image running on Ubuntu 22.04 LTS pinned to version `2023-03-27`](https://hub.docker.com/layers/jupyter/scipy-notebook/2023-03-27/images/sha256-e791e5ba6c03fdb1303272059256fc53ed5fd8073656ea2f2b542a784dbe7df3?context=explore) to create a [development container](https://code.visualstudio.com/docs/devcontainers/containers) to run our experiments.

- `notebooks/GenSVM-demo.ipynb` provides an interactive widget to play around with the GenSVM parameters on the Iris flower data set as well as the results of the grid search.
- In `notebooks/Parameter-Demo.ipynb` we generate a custom data set to illustrate the effects of varying the parameter `p`.
- `notebooks/GenSVM-simple-demo.ipynb` contains the plots used in the introduction of Chapter 3.