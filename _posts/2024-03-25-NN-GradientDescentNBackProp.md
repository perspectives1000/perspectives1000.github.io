---
title: Comparing Gradient Descent and Back Propogation
date: 2024-03-25
categories: [generativeAI]
tags: [general]
author: perspectives1000
---

### Comparing Gradient Descent and Back Propogation in Neural Networks

| Feature | Gradient Descent | Backpropagation |
| --- | --- | --- |
| Goal | Minimize the cost function (error) of the neural network | Efficiently calculate gradients needed by gradient descent |
| Method | Uses the concept of gradients to find the direction of steepest descent in the cost function | Employs chain rule to calculate the contribution of each weight to the overall error |
| Process | 1. Starts with random weights. <br> 2. Feeds data, calculates loss. <br> 3. Calculates gradients of loss w.r.t. weights. <br> 4. Adjusts weights in the negative direction of gradient (learning rate). <br> 5. Repeats for all data. | 1. Performs forward pass (activations through network). <br> 2. Calculates error at output layer. <br> 3. Performs backward pass (propagates error backwards). <br> 4. Calculates gradients using chain rule. |
| Analogy | Finding the lowest valley in a hilly landscape (cost function) | Pinpointing the most efficient path down the hill |
| Generality | More general optimization technique | Specifically designed for neural networks |
| Role | Driver | Navigator |

**Works Together:** Gradient descent uses the gradients provided by backpropagation to update the weights in the neural network, ultimately leading to better predictions.


----
**Reference:** Gemini
