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


where (Z_i) is the logit for class (i).

---

### Loss Function

Cross-entropy loss for one-hot labels:

[
\text{Loss} = -\frac{1}{m} \sum_{i=1}^{m} \sum_{j=1}^{C} Y_{j,i} \log(\hat{Y}_{j,i})
]

* (m) = number of samples
* (C) = number of classes (10)
* (Y) = true labels
* (\hat{Y}) = predicted probabilities

**Accuracy:**

[
\text{Accuracy} = \frac{\text{Number of Correct Predictions}}{\text{Total Samples}}
]

---

### Backward Pass (Gradient Descent)

For a dense layer:

[
dW = \frac{1}{m} dZ \cdot X^T
]
[
db = \frac{1}{m} \sum dZ
]
[
dX = W^T \cdot dZ
]

**Weight update:**

[
W := W - \text{learning_rate} \cdot dW
]
[
b := b - \text{learning_rate} \cdot db
]

**Softmax + Cross-Entropy Simplified Gradient:**

[
dZ = \hat{Y} - Y
]

**ReLU gradient:**

[
dX = dZ \quad \text{if } Z > 0, \quad 0 \text{ otherwise}
]

---

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/mnist-nn-numpy.git
cd mnist-nn-numpy
```

2. Run the notebook or script:

```bash
python mnist_nn_numpy.py
```

3. Training will print **loss and accuracy** for each iteration.
4. At the end, **test accuracy** is printed.

---

## Example Output

```
iteration 100/100 - Loss: 0.5110 - Accuracy: 0.8686
Test Accuracy: 0.8652
```

---

## Notes

* Input is **transposed** to `(features, samples)` for proper matrix multiplication.
* Learning rate is **dynamically adjusted** as `learning_rate = 0.2 * loss`.
* This project demonstrates foundational knowledge of neural networks and backpropagation.
* Suitable as a **portfolio project** to show your deep understanding of ML fundamentals.

---

## License

MIT License

```

This README:  

- Includes **all math formulas** for forward, backward passes, and loss.  
- Explains **why transposes and learning rate adjustment** are used.  
- Is **portfolio-ready**, clearly showing your understanding.  

If you want, I can also make a **super polished GitHub version with badges and TOC** that looks very professional.  

Do you want me to do that too?
```
