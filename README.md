# Open Competition
## General

This is a library that aims to provide a uniform interface for common data competition or, more generally, for predictive modeling. In general, four areas 
will be covered. 

1. Tabular data mining.
2. NLP related tasks.
3. CV related tasks.
4. AutoML: RL and Neural Architecture Search.

### General Functionality
The following functionalities have already been implemented. 

1. A general framework for training neural networks. This is adapted from 
HuggingFace Transformer(https://github.com/huggingface/transformers.git). However, some changes are made so that it accepts general PyTorch models.


### Tabular Data Mining
The following functionalities have already been implemented. 

1. Encoders: This module contains commonly used encoders to transform discrete and continuous variables into different forms. This module also includes dimension reduction
functionalities, mainly PCA and tSNE. Note that in this module, unlike sklearn conventions, 
we directly create names for the newly generated variables (might need to be changed).
2. Model Fitter: This module provides a model fitter for XgBoost, LightGBM, CatBoost, 
Logistic Regression, KNN, Random Forest (based on LGB implementation), and SVM.
The model fitter allows for easy training and cross-validation. For hyperparameter search,
we have wrapped hyperopt, which performs sequential Bayesian search. Some default search spaces
have been provided. 
3. Functions to find maximal linear dependent sets. Note that this part is written in C++. 

## Future Implementation Plans
Based on priorities, the following functionalities will be added. 

1. Variable selection methods for tabular data. 
2. Deep learning methods for tabular data. Include entity embeddings, variations of transformers, FM models.
3. TabNet and associated NAS methods. Currently, only a differentiable version (https://arxiv.org/abs/1910.04465) will 
be implemented. 
4. More optimizers for the general deep learning framework.
5. Adversarial training methods for deep learning. 
6. Unsupervised data augmentation (only for classification problems; see https://arxiv.org/abs/1904.12848 for details).
7. DAE and common VAE for tabular data. 
8. A general framework for training Electra (https://arxiv.org/abs/2003.10555) type pretrained model. 

After all these have been implemented, NLP related tasks will be implemented. 

NOTE: These plans are only for provisioning. If one would like to make new requests, please post in the issues session. Better yet, we appreciate any contribution, especially in reinforcement learning algorithms, 
CV and neural architecture search.  
