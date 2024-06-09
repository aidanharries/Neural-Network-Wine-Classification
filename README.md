# Neural Network: Wine Classification

## Introduction

In this project, I explore the basics of Neural Networks using PyTorch by classifying wines from the Wine dataset, which is part of the sklearn library. The goal is to predict wine classes based on various features. The dataset comprises chemical constituents of wines grown in the same region in Italy but derived from three different cultivars (types of grape plants). The dataset includes 13 features and a target label representing the wine's class. The classes are as follows:

- Class 0: Wine from the first cultivar
- Class 1: Wine from the second cultivar
- Class 2: Wine from the third cultivar

Although this task is traditionally approached as a classification problem, I have framed it as a regression task by converting the class labels to floating-point numbers.

## Setup and Data Loading

First, necessary libraries are imported, and the data is loaded. The Wine dataset is split into training and test sets, and the features are standardized, ensuring all features contribute equally to model training.

## Data Conversion to PyTorch Tensors

The data is then converted to PyTorch tensors, the primary data structure used in PyTorch for storing multidimensional arrays.

## Neural Network Model

### Basic Model

A simple two-layer neural network is defined:

- **Layer 1:** A linear layer that transforms the input features.
- **ReLU Activation:** Adds non-linearity.
- **Layer 2:** Another linear layer that outputs the regression prediction.

### Training the Basic Model

The basic model is trained using the Mean Squared Error (MSE) loss function and the Adam optimizer. The model undergoes multiple epochs of training, with periodic evaluation on the test set.

### Evaluating the Basic Model

After training, the model is evaluated on the test set to compute the loss, providing an initial performance assessment.

### Predictions from Basic Model

The predictions from the basic model are compared to the true values to visually assess accuracy.

## Enhanced Neural Network Model

### Enhanced Model Design

An enhanced model with additional layers and non-linear activation functions is designed:

- **Layer 1:** Linear layer followed by ReLU.
- **Layer 2:** Another linear layer followed by ReLU.
- **Layer 3:** A final linear layer for output.

### Training the Enhanced Model

The enhanced model includes L2 regularization (weight decay) and a learning rate scheduler for better convergence. The training procedure remains similar to the basic model but with these added enhancements.

### Evaluating the Enhanced Model

The enhanced model is evaluated on the test set to compute the loss, showing improved performance compared to the basic model.

### Predictions from Enhanced Model

The predictions from the enhanced model are compared to the true values, demonstrating more accurate and closer predictions.

## Conclusion

This project provided an in-depth look at building, training, and evaluating neural networks using PyTorch. Starting with a basic two-layer model, I progressed to a more complex architecture. The enhanced neural network, featuring additional layers, non-linear activation functions, L2 regularization, and a learning rate scheduler, demonstrated a notable improvement in performance.

While the Wine dataset is inherently categorical and a classification approach might be more suitable, this project effectively illustrates the capabilities of neural networks and the versatility of PyTorch. Future work could explore classification models, compare their effectiveness with the regression models developed here, and experiment with advanced neural network architectures and training techniques.
