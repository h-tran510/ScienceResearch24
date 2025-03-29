# Drug Toxicity Classification With Graph Attention Networks

This is the code behind the project of the same name, which was presented at the 2025 LA County Science and Engineering Fair (LACSEF) in the category of pharmacology. 

# Abstract

## Rationale and Objectives
In drug development, 90% of drugs fail, and 30% of drug failures are due to unmanageable toxicity or side effects. Toxicity in particular is an overlooked factor in in-silico drug discovery, with clinical efficacy often being prioritized. Machine learning algorithms like Graph attention networks (GATs) use graphs as a data representation, which are able to model the complexity of heterogeneous structures like molecules, making it ideal for determining drug properties like toxicity. A GAT was built to classify drug toxicity by extracting features indicative of drug toxicity from data.

## Methods
Python in Google Colab was used to code the project. The Toxcast open source dataset is used, consisting of SMILES strings as well as binary toxicity labels, with 10 features selected based on their data distribution. The model’s architecture is based upon the pre-existing HiGNN model, which uses a feature attention layer, a neural tensor network layer, and a custom GNN model. It runs across each of the 10 features for 200 epochs.

## Results 
The AUC of the best performing feature (Feature: NCCT_TPO_GUA_dn) according to AUC is 0.8, the precision is 0.75, the recall is 1, the accuracy is 0.82. This occurred at the 90th  epoch at 20.98 seconds. Despite the model’s high accuracy and AUC, showing it is able to predict the right classes and differentiate between positive and negative classes, and instability behind the accuracy and the loss curves shows that the model is overfitting. Its low precision and high recall also suggests that the model identifies positive cases well, yet it incorrectly labels negative cases, showing class imbalance. 

## Conclusions
The model needs further refinement to allow it to generalize well across new samples by further implementing regularization techniques and by increasing the size of the dataset. In the future, work can be done to model the intensity of such drug effects as well as possible responses to specific dosages. Graph neural networks are still a relatively new type of algorithm, so more research can be done to optimize these algorithms and to improve interpretability.

## Extra Notes
Due to the size limits for my Github uploads, all of the results are available here: https://drive.google.com/drive/folders/15uzPWTv1vfebAmRkEQqbCDXodHWHLoH9?usp=sharing. This folder contains the 10 different features that were tested alongside figures for its loss curves, accuracy curves, a confusion matrix for training, and a confusion matrix for testing. There is also a document for each titled "metrics.txt" that detail each metric and the epoch at which they occurred. 

I could only test with 10 different features at the time of me doing this project due to software limitations and time constraints.

## Acknowledgements

I would like to thank my mentor, Noam Grunfeld, for helping me navigate my journey with my first research project. She helped me greatly in improving my understanding of the overall steps of the research process and in developing a machine learning model, and she helped guide me when building the baseline neural network model. 

