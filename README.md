# MNIST Neural Network from Scratch

This repository contains a **from-scratch implementation of a neural network** using **NumPy** to classify handwritten digits from the **MNIST dataset**.

## Features

- Fully connected (dense) layers implemented from scratch  
- ReLU and Softmax activation functions  
- Cross-entropy loss  
- Backpropagation and gradient descent  
- Training and testing on MNIST dataset  

## Requirements
- NumPy  
- scikit-learn  
- pandas  
## Dataset

The MNIST dataset is loaded via scikit-learn
* Features are normalized to [0, 1]
* Labels are one-hot encoded using oneHotEncoder
* Data is split into **train (70%)** and **test (30%)** sets

## Neural Network Architecture

The network has **2 layers**:

1. **Dense Layer 1:** 128 neurons, ReLU activation
2. **Dense Layer 2:** 10 neurons, Softmax activation (for 10 digit classes)

### Forward Pass Math

For a dense layer:

* (X) = input matrix 
* (W) = weights matrix 
* (b) = biases 
* Z = W * X + b


**ReLU Activation**
ReLU(Z) = max(0, Z)

**Softmax Activation:**

Softmax(Z_i) = (e^(Z_i))/(sum_j e^{Z_j))


### Loss Function
Cross-entropy loss

## Resources

The following resources helped me understand neural networks and construct this project.

- [Neural Networks from Scratch – 3Blue1Brown](https://www.youtube.com/watch?v=aircAruvnKk)
- [Backpropagation Explained – StatQuest](https://www.youtube.com/watch?v=Ilg3gGewQ5U)
- [Building a neural network FROM SCRATCH (no Tensorflow/Pytorch, just numpy & math)](https://youtu.be/w8yWXqWQYmU?si=97QwX6nf54qQqdu6)

