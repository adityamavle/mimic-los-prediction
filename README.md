# Hospital Length of Stay Prediction Notebook

## Overview

This notebook aims to predict the Length of Stay (LOS) of patients in a hospital using a neural network model. In healthcare, LOS prediction is crucial for resource allocation, bed management, and patient care planning. The dataset used is the Open Access MIMIC Clinical Dataset 

## LOS Prediction Problem

The primary goal of this notebook is to build a predictive model that can accurately estimate the Length of Stay (LOS) for future patients. This is a regression problem where the model will learn to predict a numerical value (LOS in days) based on the input features from the dataset. Accurate LOS predictions can help hospitals optimize resource allocation, improve patient flow, and enhance overall healthcare management.

## v1

### Neural Network Model

- A deep neural network with multiple layers (256-128-64-32-1) was constructed for Length of Stay (LOS) prediction.
- The model uses ReLU activation functions between layers.
- Mean Squared Error (MSE) was employed as the loss function.
- Adam optimizer with a learning rate of 0.001 was used for model optimization.
- A learning rate scheduler with patience of 5 was implemented to adjust the learning rate during training.
- Early stopping with a patience of 10 epochs was employed to prevent overfitting.

### Training and Evaluation

- The model was trained for a maximum of 100 epochs.
- Training data was divided into batches of 64 samples and shuffled during training.
- The training loop monitored the training loss and applied early stopping if no improvement occurred.
- The training loss plot shows the progress of the loss over epochs.

### R^2 Score

- After training, the model was evaluated on a separate test dataset.
- The model achieved an R^2 score of 0.782 on the test data.
- An R^2 score of 0.782 indicates that the model explains a substantial portion of the variance in LOS predictions, suggesting good predictive performance.

In conclusion, this version (v1) of the neural network model demonstrates promising results with an R^2 score of 0.782, indicating its effectiveness in predicting Length of Stay (LOS) for hospital patients.
