# COSYNE 2023 Workshop on Generative Models

*What I cannot create I do not understand: analyzing neural and behavioral data with generative models*

## Introduction

A central goal of systems neuroscience is to understand how high-dimensional neural activity relates to complex stimuli and behaviours. Recent advances in neural and behavioural recording techniques have enabled routine collection of large datasets to answer these questions. With access to such rich data, we are now able to describe activity at the level of neural populations rather than individual neurons, and we can look at the neural underpinnings of increasingly complex and naturalistic behaviours. Unfortunately, it can be challenging to extract interpretable structure from such high-dimensional, often noisy, data. Generative modelling is a powerful approach from probabilistic machine learning that can reveal this structure by learning the statistical properties of the recorded data, often under the assumption that the high-dimensional observations arise from some lower-dimensional ‘latent’ process. Moreover, constructing such generative models makes it possible to build prior knowledge about the data directly into the analysis pipeline, such as multi-region structure or temporal continuity. This makes it possible both to make more efficient use of the available data by building in appropriate inductive biases, and to make the models more interpretable by shaping them according to the known structure of the data. Given the wealth of advances in generative modelling for systems neuroscience in recent years, we think the time is ripe to review this progress and discuss both challenges and opportunities for the future.




## Generative models

- **iLQR-VAE** ([Schimel et al., 2022](https://www.biorxiv.org/content/10.1101/2021.10.07.463540v2.abstract))
- **Scalable Bayesian GPFA** ([Jensen et al., 2021](https://proceedings.neurips.cc/paper/2021/hash/58238e9ae2dd305d79c2ebc8c1883422-Abstract.html))
- **Universal count model** ([Liu and Lengyel, 2021](https://proceedings.neurips.cc/paper/2021/hash/6f5216f8d89b086c18298e043bfe48ed-Abstract.html))
- **Manifold GPLVM** ([Jensen et al., 2020](https://proceedings.neurips.cc/paper/2020/hash/fedc604da8b0f9af74b6cfc0fab2163c-Abstract.html))

Other models...



## Run locally 💻 

Follow the instructions below to install the software that is
necessary to run the notebooks on your own computer.

First, set up a virtual environment with Python 3, activate it 
and install packages:

```
python3 -m venv /path/environment
. /path/environment/bin/activate
python3 -m pip install -r requirements.txt
```

More detailed instructions are provided further below.


### Detailed instructions

Click on a section to expand it.

<details>
<summary>1. <b>Install Python 3</b></summary>

- On Windows: ...
  
- On MacOS, Ubuntu, etc, go to 'Terminal' and run `chmod +x` on the downloaded `.sh` file, then run it
  with...
</details>



## Acknowledgements

We would like to thank the COSYNE Workshops organizing committee...



## Citing this

Please cite the Zenodo DOI.

[![DOI](https://zenodo.org/badge/451483302.svg)](https://zenodo.org/badge/latestdoi/451483302)