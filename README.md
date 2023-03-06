# COSYNE 2023 Workshop on Generative Models

*What I cannot create I do not understand: analyzing neural and behavioral data with generative models*

[Website](https://sites.google.com/cam.ac.uk/cosyne-generative-workshop/)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7701723.svg)](https://doi.org/10.5281/zenodo.7701723)

## Introduction

A central goal of systems neuroscience is to understand how high-dimensional neural activity relates to complex stimuli and behaviours. Recent advances in neural and behavioural recording techniques have enabled routine collection of large datasets to answer these questions. With access to such rich data, we are now able to describe activity at the level of neural populations rather than individual neurons, and we can look at the neural underpinnings of increasingly complex and naturalistic behaviours. Unfortunately, it can be challenging to extract interpretable structure from such high-dimensional, often noisy, data. Generative modelling is a powerful approach from probabilistic machine learning that can reveal this structure by learning the statistical properties of the recorded data, often under the assumption that the high-dimensional observations arise from some lower-dimensional ‘latent’ process. Moreover, constructing such generative models makes it possible to build prior knowledge about the data directly into the analysis pipeline, such as multi-region structure or temporal continuity. This makes it possible both to make more efficient use of the available data by building in appropriate inductive biases, and to make the models more interpretable by shaping them according to the known structure of the data. Given the wealth of advances in generative modelling for systems neuroscience in recent years, we think the time is ripe to review this progress and discuss both challenges and opportunities for the future.


## Example notebooks

We provide three example notebooks which implement and discuss a range of generative models commonly used in neuroscience.

**1. Regression**\
This notebook considers methods used for regression - the case where we have both some observations and set of regressors that we think can predict our observations.
We start from the simple case of linear regression and reformulate it as a Bayesian method, which can be generalized to the more complicated but powerful *Gaussian process* regression (see this [video](https://www.youtube.com/watch?v=cQAPIlMeL_g) for a more thorough overview of the use of Gaussian processes in systems neuroscience).

**2. Latent variable models (lvms)**\
Having treated the case of regression, we then move on to latent variable models. This *unsupervised learning* setting generalizes regression to the case where we do now know the regressors but instead have to *infer* them from the data.
This inference process is often complicated, which calls for simplifying assumptions such as Gaussianity or linearity.
In this notebook, we consider both linear and non-linear method and look at the importance of such modelling choices when analysing high-dimensional data.

**3. Discrete state spaces**\
In both of the above cases, we worked with *continuous* state spaces.
However, it is becoming increasingly common in systems neuroscience to also work with discrete state spaces, such as motivational states or different regimes of neural dynamics.
In this notebook, we start from the simple Hidden Markov Model for inferring discrete states and transitions from data and then generalize to the increasingly popular approach of Switching Linear Dynamical Systems for modelling neural data.

<details>
<summary><b>Instructions to run locally 💻 </b></summary>

To run the notebooks, we need to install software dependencies in Python 3 (3.7 or higher). Note for Windows one has to [do some more work](https://github.com/cloudhan/jax-windows-builder) to install JAX. Open the terminal: 
    
1. Create a Python 3 virtual environment in a directory of your choice 

```
mkdir /path_to_environment/
python3 -m venv /path_to_environment/
```
    
2. Activate the new environment 
    
```
. /path_to_environment/bin/activate
```
    
3. Install the required dependencies 
    
```
python3 -m pip install -r requirements.txt
```
    
4. Add the new environment to Jupyter kernels 

```
python3 -m ipykernel install --user --name=cosyne_2023
```
    
5. We also make use of the [mgplvm](https://github.com/tachukao/mgplvm-pytorch/tree/cosyne2023) and [ssm](https://github.com/lindermanlab/ssm) libraries, which can be installed from 

```
cd ..
python3 -m pip install git+https://github.com/tachukao/mgplvm-pytorch@cosyne2023
git clone https://github.com/lindermanlab/ssm.git
cd ssm
python3 -m pip install numpy cython
python3 -m pip install -e .
cd ../cosyne-2023-generative-models/
```
   
6. Now one should be able to run the notebooks with all dependencies available using the `cosyne_2023` IPython kernel.
    
</details>



## Literature

- **Review of linear Gaussian LVMs** ([Roweis & Ghahramani, 1999](https://ieeexplore.ieee.org/abstract/document/6790691))
- **Gaussian process factor analysis** ([Yu et al., 2009](https://proceedings.neurips.cc/paper/2008/hash/ad972f10e0800b49d76fed33a21f6698-Abstract.html))
- **Bayesian GPFA** ([Jensen et al., 2021](https://proceedings.neurips.cc/paper/2021/hash/58238e9ae2dd305d79c2ebc8c1883422-Abstract.html))
- **Gaussian process latent variable models** ([Wu et al., 2017](https://proceedings.neurips.cc/paper/2017/hash/b3b4d2dbedc99fe843fd3dedb02f086f-Abstract.html))
- **Manifold GPLVMs** ([Jensen et al., 2020](https://proceedings.neurips.cc/paper/2020/hash/fedc604da8b0f9af74b6cfc0fab2163c-Abstract.html))
- **Universal count model** ([Liu and Lengyel, 2021](https://proceedings.neurips.cc/paper/2021/hash/6f5216f8d89b086c18298e043bfe48ed-Abstract.html))
- **LFADS** ([Pandarinath et al., 2018](https://www.nature.com/articles/s41592-018-0109-9)) 
- **iLQR-VAE** ([Schimel et al., 2022](https://www.biorxiv.org/content/10.1101/2021.10.07.463540v2.abstract))

- **Bayesian Learning and Inference in Recurrent Switching Linear Dynamical Systems** ([Linderman et al., 2017](https://proceedings.mlr.press/v54/linderman17a.html))


## Acknowledgements

We would like to thank the COSYNE Workshops organizing committee for giving us the opportunity to run our Workshop in Montreal.
We are also grateful to Ta-Chu Kao, Guillaume Hennequin, Máté Lengyel, and many others in CBL and beyond for various discussions and assistance with implementations of some of the methods.


## Citing this

Please cite the Zenodo DOI.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7701723.svg)](https://doi.org/10.5281/zenodo.7701723)