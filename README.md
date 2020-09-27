# MachineLearning

## Setup
Please run the following commands after forking the repo:

pip install scipy
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn 

Then run script.py. 

## Project Aim

The aim of this project is to classify iris flowers among three species (setosa, versicolor, or virginica) from measurements of sepals and petals' length and width. The iris data set contains 3 classes of 50 instances each, where each class refers to a type of iris plant.

## Methodology

In order to do this the dataset must first be visualised via graphs and box plots, and statistical information on the value distribution (standard deviations, 25 and 50 percentile boundaries).

Six different alogrithms were attempted to produce a predictive model for iris flowers based on petal information in the dataset, these are as follows:

Logistic Regression (LR)
Linear Discriminant Analysis (LDA)
K-Nearest Neighbors (KNN).
Classification and Regression Trees (CART).
Gaussian Naive Bayes (NB).
Support Vector Machines (SVM)

Some of the data was removed from the dataset that the algorithms will not get to see and we will use this data to get a second and independent idea of how accurate the best model might actually be.

We will split the loaded dataset into two, 80% of which we will use to train, evaluate and select among our models, and 20% that we will hold back as a validation dataset.

Additionally a stratified 10-fold cross validation approach was used to estimate model accuracy.

This split our dataset into 10 parts, train on 9 and test on 1 and repeat for all combinations of train-test splits.

Stratified means that each fold or split of the dataset will aim to have the same distribution of example by class as exist in the whole training dataset.

It was determined that the Support Vector Machines alogrithm produced the most accurate model, 

LR: 0.960897 (0.052113)
LDA: 0.973974 (0.040110)
KNN: 0.957191 (0.043263)
CART: 0.957191 (0.043263)
NB: 0.948858 (0.056322)
SVM: 0.983974 (0.032083)

The SVC model was then fit to the entire training dataset and make predictions on the validation dataset.

Finally, the classification report provides a breakdown of each class by precision, recall, f1-score and support showing excellent results (granted the validation dataset was small).
