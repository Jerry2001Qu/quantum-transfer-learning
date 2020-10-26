
# Transfer learning in hybrid classical-quantum neural networks
A transfer learning approach applied to hybrid neural networks composed of classical and quantum elements.

This repository contains the source code related to the research paper *"Transfer learning in hybrid classical-quantum neural networks"* [arXiv:1912.08278](https://arxiv.org/abs/1912.08278) (2019).

![Figure](static/figure_c2q_notebook.png)

## Contents
* `dressed_circuit.ipynb`: Jupyter notebook to train and test a _dressed_ variational quantum circuit for the classification of a syntetic dataset of 2-dimensional points (spirals).

* `c2q_transfer_learning_ants_bees.ipynb`: Jupyter notebook to train and test a hybrid neural network for the classification of high-resolution images (_ants_ and _bees_). This example is based on a classical-to-quantum (CQ) transfer learning approach.

* `c2q_transfer_learning_cifar.ipynb`: Jupyter notebook to train and test a hybrid neural network for the classification of CIFAR images, e.g., _dogs_ vs. _cats_ or _planes_ vs. _cars_. This example is based on a classical-to-quantum (CQ) transfer learning approach.

* `q2c_transfer_learning.ipynb`: Jupyter notebook to train and test a hybrid neural network for the classification of continuous variable quantum states. This example is based on a quantum-to-classical (QC) transfer learning approach.

* `q2q_transfer_learning.ipynb`: Jupyter notebook to train and test a hybrid neural network for the classification of continuous variable quantum states. This example is based on a quantum-to-quantum (QQ) transfer learning approach.

* `quantum_processors\`: folder containing the code to experimentally classify high-resolution images (_ants_ and _bees_) with real quantum processors (IBM and Rigetti). The same model can be numerically simulated with the notebook `c2q_transfer_learning_ants_bees.ipynb`.

* `pre_trained\`: folder containing pre-trained variational parameters saved as NumPy files. They are loaded by the notebooks `q2q_transfer_learning.ipynb` and `q2q_transfer_learning.ipynb`.

* `static\`: folder containing some static images.

* `supplementary_simulations\`: folder containing additional notebooks for testing the _dressed_ quantum circuit model with different datasets and for simulating two classical models which are similar to the hybrid model used in `c2q_transfer_learning_ants_bees.ipynb`.

## Usage

To visualize the content of the Jupyter notebooks without running the code there are two alternatives:
1. Navigate with a browser to the GitHub repository and simply click on the notebook file. GitHub will automatically visualize the notebook, however the rendering may not be good (especially for LaTeX formulas).
2. Copy the URL of the notebook file and paste it into [nbviewer](https://nbviewer.jupyter.org).

To open and run a local copy of a notebook one should apply the following steps:

1. If missing, install [JupyterLab](https://jupyter.org/install).
2. Run the command:
```
$ jupyter notebook
```
3. Navigate to the local notebook file and open it.

For the usage of the code in `quantum_processors\` see the dedicated README file `quantum_processors\README.md`.

## Requirements

#### Software
All notebooks require the installation of JupiterLab with a Python 3 kernel. In addition the library matplotlib is required for generating plots and images.

The notebook `dressed_circuit.ipynb` requires the Python library PennyLane.

The notebooks `c2q_transfer_learning_*.ipynb` require the Python libraries PennyLane and PyTorch.

The notebooks `q2c_transfer_learning.ipynb` and  `q2q_transfer_learning.ipynb` require the library Strawberry Fields with the TensorFlow backend.

Notebooks can be run using the package versions specified in the `requirements.txt` file.

For the requirements of the code in `quantum_processors\` see the dedicated README file `quantum_processors\README.md`.

#### Datasets
The notebook `c2q_transfer_learning_ants_bees.ipynb` and the code in `quantum_processors\` require to manually download the dataset, consisting of the _Hymenoptera_ subset of ImageNet (ants and bees). The dataset can be downloaded [here](https://download.pytorch.org/tutorial/hymenoptera_data.zip) and should extracted in the subfolder `\data\hymenoptera_data\`.

The notebook `c2q_transfer_learning_cifar.ipynb` will automatically download the CIFAR10 dataset.

The datasets (random quantum states) for the notebooks `q2q_transfer_learning.ipynb` and `q2q_transfer_learning.ipynb` are automatically generated on the fly, during the training and testing phases.

## Authors

Andrea Mari, Thomas R. Bromley, Josh Izaac, Maria Schuld, and Nathan Killoran.

If you are doing any research using this source code, please cite the following paper:

> Andrea Mari, Thomas R. Bromley, Josh Izaac, Maria Schuld, and Nathan Killoran. _Transfer learning in hybrid classical-quantum neural networks_. [arXiv:1912.08278](https://arxiv.org/abs/1912.08278) (2019).

## License

This source code is free and open source, released under the Apache License, Version 2.0.
