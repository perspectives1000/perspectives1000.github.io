---
title: Machine Learning Basics
date: 2024-02-01
categories: [generativeAI]
tags: [general]
author: perspectives1000
---

### Introduction
Machine learning is the practice of helping software perform a task without explicit programming or rules. With traditional computer programming, a programmer specifies rules that the computer should use. ML requires a different mindset, though. Real-world ML focuses far more on data analysis than coding. Programmers provide a set of examples and the computer learns patterns from the data. You can think of machine learning as “programming with data”.

In basic terms, ML is the process of training a piece of software, called a model, to make useful predictions  (inferences) or generate content from data.

There are multiple steps in the process of getting answers from data using ML. For a step-by-step overview, check out this **[guide](https://developers.google.com/machine-learning/guides/text-classification/)** that shows the complete workflow for text classification, and describes important steps like collecting a dataset, and training and evaluating a model with TensorFlow or Pytorch.

**Data → Model → Training → Evaluating → Inference**

### Types of learning in ML systems and use-cases

Prompt: Format by type and use-cases

Machine learning can be categorized based on how they learn from data. Here's a breakdown of the main types and their use cases:

**1. Supervised Learning (Labeled Data):**

- **Subcategories:**
    - **Regression:** Predicts continuous outputs (**numbers**) like stock prices or house prices. (Ex: Forecasting sales trends);  A weather model that predicts the amount of rain, in inches or millimeters.
    - **Classification:** Categorizes data points into **predefined classes**. (Ex: Spam filtering, Image recognition)
        - **Binary** classification - Ex:  Predict ‘Rain’ or ‘No Rain’
        - **Multiclass** classification - Ex:  Label output as ‘rain’, ‘hail’, ‘snow’ or ‘sleet’
- **Use Cases:**
    - Recommendation systems (suggesting products or content)
    - Fraud detection (identifying suspicious financial activity)
    - Medical diagnosis (analyzing medical scans)
    - Self-driving cars (interpreting sensor data for navigation)

**2. Unsupervised Learning (Unlabeled Data):**

- **Subcategories:**
    - **Clustering:** Groups similar data points together. (Ex: Customer segmentation, Document clustering). (No pre-defined classes unlike in classification)
    - **Dimensionality Reduction:** Reduces complex data to a lower dimension for easier analysis. (Ex: Image compression, Anomaly detection)
- **Use Cases:**
    - Market research (understanding customer behavior)
    - Anomaly detection (finding unusual patterns in network traffic)
    - Scientific discovery (identifying patterns in large datasets)
    - Image segmentation (separating objects in an image)

**3. Reinforcement Learning (Trial and Error):**

- **Subcategories:**
    - **Model-based:** Learns a model of the environment to make decisions.
    - **Model-free:** Learns through direct interaction with the environment.
- **Use Cases:**
    - Robotics control (learning to walk or manipulate objects)
    - Game playing (learning to play complex games like chess)
    - Resource allocation (optimizing resource usage in a network)
    - Traffic light control (dynamically adjusting traffic flow)

**4. Semi-supervised Learning (Labeled & Unlabeled Data):**

- **Subcategories:** Combines supervised and unsupervised learning techniques.
- **Use Cases:**
    - When labeled data is scarce but unlabeled data is abundant. (Ex: Sentiment analysis on social media)
    - Image classification with limited labeled images.
    - Text classification for spam filtering with a small set of labeled spam emails.

**5. Self-supervised Learning (Unlabeled Data - Specific Task):**

- **Subcategories:** Models create their own labels or signals from unlabeled data relevant to a specific task.
- **Use Cases:**
    - Natural Language Processing (understanding and generating human language)
    - Machine translation (translating languages without paired examples)
    - Speech recognition (converting spoken language to text)
    - Image captioning (generating descriptions of images)
 
### Various Learning styles

  - **Neural Networks:** Mimic the brain for complex pattern recognition in images, speech, or text. (Ex: Facial recognition).  **They consist of interconnected nodes that process information layer by layer.**
      
  - **Support Vector Machines (SVMs):** Draw the best line to separate data categories. (Ex: Image classification, handwriting recognition).    - Supervised Learning model for classification
      
      A support vector machine (SVM) is a supervised machine learning algorithm that classifies data by finding an **optimal line or hyperplane** that maximizes the distance between each class in an N-dimensional space.
      
  - **Decision Trees:** Ask a series of questions about data to make a prediction, like a flowchart. (Ex: Customer churn prediction, Medical diagnosis). **These models work like flowcharts**, asking a series of questions about the data to make a prediction.  They are easy to interpret and don't require massive amounts of data for training.  Non-parametric Supervised learning for classification and regression.
      
  - **K-Nearest Neighbors (KNN):** Classify data based on similarity to its closest neighbors. (Ex: Handwritten digit recognition). Non-parametric Supervised learning classifier model
      
  - **Ensemble Models:** Combine multiple models for improved performance, like a team of experts. (Ex: Gradient boosting for fraud detection, random forest for stock market prediction)

---
**Reference** : https://www.tensorflow.org/about
