# CNAPs for regression
The network consists of two sub-networks:
1. Target network: an MLP regressor predicting output based on input, and 
2. Adaptation Network: a MLP network leveraging the current task's dataset as context and the activations of the previous layers of the Target Network to modulate its activations of each layer for adapting to the current task.

It is implemented in three stages, namely:
1. Base Model: a basic MLP to establish the Target Network.
2. CNAPs without Autoregressive: consists of an adaptive set encoder to accommodate varying numbers of context points, and encoded output goes to the Adaptation Network and modulate the weights of the Target Network.
3. CNAPs with Autoregressive: consists set encoders for each layer of the Target Network whose output goes to the Adaptation Network and modulate the weights of the Target Network.


# CNAPs for Multi-Task Few-shot Classification
We replicated the [CNAPs: Fast and Flexible Multi-Task Classification Using Conditional Neural Adaptive Processes](https://github.com/cambridge-mlg/cnaps) and evaluated its performance accross various datasets. 

## Datasets used:
Curated 3 completely new datasets using CelebA and Stanford Cars dataset, such that it becomes a n-class classification problem. The datasets are as follows:
- Celeb10
- CelebFace150
- CelebCars

Along with the above datasets, we also used the following datasets:
- CIFAR-10
- CIFAR-100

The details of precedure, inference and results can be found in the [presentation](https://github.com/RYeeshuDhurandhar/cnaps/blob/main/presentation.pdf) and [report](https://github.com/RYeeshuDhurandhar/cnaps/blob/main/report.pdf).

# Other collaborators:
- Bhavesh Jain
- Dhairya Shah
- Lipika Rajpal
- Rahul Chembakasseril

# Mentors:
- Prof. Nipun Batra
- Madhav Kanda
- Sarth Dubey
