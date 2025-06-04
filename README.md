# Multi-Objective Automatic Discovery of Optimized Metamaterials for Varying Velocity Impact Protection
This repository contains the code for a strain-rate-aware active deep learning framework enabling multi-objective optimization of impact protection lattice architectures.

Below is a quick-start tutorial for training the forward surrogate model and running the genetic optimization.

## Quick Run
### Installation
To conduct similar analyses as in the paper, begin by cloning this repository:
```
git clone https://github.com/anishsatpati/Impact-Protection-Metamat.git 
```
Please ensure you have the below dependencies:

```
pip install torch numpy matplotlib scikit-learn
```
Next, download the data and set the path to the dataset in the ```Surrogate_forward_model.ipynb``` file.

To reproduce the forward model training results, run the model with:
```
jupyter notebook Surrogate_forward_model.ipynb
```

Ensure the weights of the model are saved in the correct directory for easy access later on.
Now that the forward model has been trained, the genetic optimization algorithm can be run.

Set the path to the dataset in the ```GA_optimization.ipynb``` file.

Load the weights of the trained forward model with: ```forward_model.load_state_dict(torch.load(PATH_TO_SAVED_WEIGHTS))``` 

To obtain the first set of optimzied lattices, run the optimization file with:
```
jupyter notebook GA_optimization.ipynb
```
