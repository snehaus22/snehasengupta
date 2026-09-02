---
layout: post
title: Breast Cancer Cell Classification using ML
description: A machine learning model with supervised and unsupervised aspects for evaluating the accurate diagnosis of breast cancer by analyzing characteristics of individual cells. Utilizing the open source Wisconsin Diagnostic Breast Cancer (WDBC) dataset, which contains various features computed from digitized images of fine needle aspirates (FNAs) of breast masses, the goal was to classify tumors as either benign or malignant.
skills: 
- Machine Learning
- OpenCV
- Tensorflow
- Neural Networks
- Binary Classification
main-image: /breastcancer.png
---

## Methods
The data underwent a comprehensive preprocessing pipeline, using StandardScaler and RandomOverSampler to normalize numerical attributes and address class imbalance respectively. The dataset was then split into training, validation, and test sets for model evaluation.
A number of machine learning methods were applied, but the ones three were ultimately utilized and compared:
- Logistic regression: a linear model for binary classification, providing a probabilistic interpretation of diagnosis.
- Support Vector Machines (SVMs): An algorithm that constructs a hyperplane or set of hyperplanes in a high-dimensional space for classification, regression, and other subsequent tasks. It aims to find the optimal boundary that maximally separates the two classes.
- Neural Networks: A deep learning approach using a multi-layer architecture. The network was designed with multiple dense layers and ReLU activation functions, culminating in a sigmoid output layer for binary classification. Hyperparameter tuning was performed to optimize performance and stability of the model, using validation loss as the primary metric.

## Results
Each model was evaluated based on standard classification metrics, including precision, recall, and F1-score, on an unseen test-set. The models demonstrated high-accuracy as shown below in distinguishing between malignant and benign cases, showcasing the potential of ML applications in early stages of cancer detection: 

{% include image-gallery.html images="mltable.png" height="400" %} 
The neural network model was extensively tuned to achieve optimal performance, highlighting the importance of interactive development in deep learning. 
{% include image-gallery.html images="mlgraph.png" height="400" %} 
