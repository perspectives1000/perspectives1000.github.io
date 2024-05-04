---
title: Neural networks - Biases, Activation and Loss functions
date: 2024-03-10
categories: [generativeAI]
tags: [general]
author: perspectives1000
---


### What are biases?

In a neural network, biases are constant values added to the weighted sum of inputs at each neuron. They play a **crucial role in influencing whether a neuron "fires"** (activates its output). Here's a breakdown of their function:

- **Understanding Weighted Sums:** Before applying an activation function, a neuron calculates a weighted sum of its inputs. Each input has a corresponding weight, which determines the strength of its influence on the neuron.
- **The Role of Bias:** The bias acts like an extra input with a weight of 1. It essentially shifts the activation function to the left or right along the horizontal axis.
- **Impact on Activation:** This shift can significantly affect the output of the neuron. A positive bias makes it easier for the neuron to activate (fire), while a negative bias makes it harder.

**Why are biases important?**

- **Overcoming Zero Threshold:** Imagine a scenario where all the weighted inputs to a neuron add up to zero. Without a bias, the activation function wouldn't budge, and the neuron wouldn't fire regardless of the input patterns. The bias term prevents this by introducing a constant value that can push the neuron towards activation or inhibition.
- **Flexibility and Learning:** Biases, along with weights, are adjusted during the training process. This allows the network to learn complex relationships in the data. By fine-tuning both weights and biases, the network can learn which features are important for activation and how sensitive a neuron should be to its inputs.

**Analogy:**

Think of a neuron like a judge in a courtroom. The weighted inputs are like pieces of evidence, and the weights represent their importance. The bias is like the judge's own baseline for making a decision (convict or acquit). A strong bias in favor of the prosecution (positive bias) might make it easier to convict, while a bias towards the defense (negative bias) might make it harder. By adjusting the weights and the bias, the judge (neuron) can reach more nuanced decisions based on the presented evidence (inputs).

### Activation functions

Activation functions are a critical part of neural networks. They **introduce non-linearity**, allowing the network to learn complex patterns in data. Here's a breakdown:

1. **Purpose:**
    - Neural networks with only linear relationships between layers wouldn't be very powerful.
    - Activation functions introduce non-linearity, enabling the network to model more intricate relationships within the data.
2. **Types of Activation Functions:**
    - There are many activation functions, each with its strengths and weaknesses. Here are a few common ones:
        - **Sigmoid:** Outputs a value between 0 and 1, often used for classification problems. (Think: Squeezing the output between 0 and 1)
        - **ReLU (Rectified Linear Unit):** Outputs the input directly if it's positive, otherwise outputs 0. Popular for its efficiency in training. (Think: Only fire if the input is positive)
        - **tanh (Hyperbolic tangent):** Outputs a value between -1 and 1, often used as an alternative to sigmoid. (Think: Squeezing the output between -1 and 1)
3. **Choosing an Activation Function:**
    - The best activation function depends on the specific task and network architecture.
    - Some factors to consider include the desired output range (e.g., probabilities between 0 and 1 for classification) and the computational efficiency of the function.
4. **Example:**
Imagine a neural network classifying handwritten digits. The activation function in the output layer might be a sigmoid function, which squishes the final output between 0 and 1, representing the probability of the input image being a specific digit (e.g., 0.9 for a highly likely 7).

### Loss function

During **[training](https://developers.google.com/machine-learning/glossary#training)** or testing, a mathematical function that calculates the loss on a **[batch](https://developers.google.com/machine-learning/glossary#batch)** of examples. A loss function returns a lower loss for models that makes good predictions than for models that make bad predictions.

The goal of training is typically to minimize the loss that a loss function returns.

Many different kinds of loss functions exist. Pick the appropriate loss function for the kind of model you are building. For example:

- **[L2 loss](https://developers.google.com/machine-learning/glossary#L2_loss)** (or **[Mean Squared Error](https://developers.google.com/machine-learning/glossary#MSE)**) is the loss function for **[linear regression](https://developers.google.com/machine-learning/glossary#linear_regression)**.
- **[Log Loss](https://developers.google.com/machine-learning/glossary#Log_Loss)** is the loss function for **[logistic regression](https://developers.google.com/machine-learning/glossary#logistic_regression)**.


---
**Reference**:  Gemini
