# Machine Learning Fundamentals (COMP 5630)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-%2334D058.svg?style=for-the-badge&logo=huggingface&logoColor=white)

## Overview
This repository contains a curated collection of foundational machine learning algorithms and predictive models implemented in Python. Completed as part of the graduate-level COMP 5630 curriculum at Auburn University, these projects bridge the gap between underlying mathematical mechanics (implementing algorithms from scratch via raw linear algebra) and modern deep learning architecture (using enterprise frameworks like TensorFlow/Keras).

## Technologies Used
* **Languages:** Python 3
* **Deep Learning & Neural Networks:** TensorFlow, Keras
* **Natural Language Processing (NLP):** Gensim (FastText), GloVe, Hugging Face Datasets
* **Mathematics & Data Manipulation:** NumPy, Pandas, Scikit-learn
* **Environment:** Google Colab, Jupyter Notebooks

## Coursework Portfolio

### [Assignment 1: Linear Regression & Ordinary Least Squares](./assignment_1_linear_regression/)
* **Core Concept:** Implementation of multiple linear regression from scratch without relying on external ML libraries.
* **Mathematical Implementation:** Solved for optimal weights using the closed-form normal equation: $\mathbf{w} = (X^\top X)^{-1} X^\top \mathbf{y}$
* **Application:** Conducted feature importance analysis and MSE evaluation on a local housing dataset to identify the most and least influential pricing factors.

### [Assignment 2: Logistic Regression & L1 Regularization](./assignment_2_logistic_regression/)
* **Core Concept:** Implementation of binary logistic regression from scratch using Gradient Ascent to maximize log-likelihood, extended to handle multi-class data using a One-vs-Rest (OvR) strategy.
* **Mathematical Implementation:** Custom optimization loop updating weights via `w = w + learning_rate * gradient`.
* **Application:** Classified cultivars in the Wine dataset. Compared the custom unregularized model against an L1-regularized model to demonstrate automated feature selection, proving that interpretability can be achieved without sacrificing accuracy.

### [Assignment 3: Convolutional Neural Networks & Age Regression](./assignment_3_cnn_age_regression/)
* **Core Concept:** Engineered a CNN architecture using TensorFlow/Keras to predict a continuous variable (age) from facial image data.
* **Technical Implementation:** Built a highly optimized `tf.data` pipeline with dynamic image augmentation. Configured a regression-specific network head using a linear output activation and Mean Squared Error (MSE) loss. 
* **Application & Analysis:** Trained and evaluated the model on the UTKFace dataset, achieving an MAE of ~6.4 years. Conducted extensive hyperparameter sweeps to evaluate optimization stability (learning rate), activation function behavior on unbounded targets (ReLU vs. Tanh), and generalization techniques (Early Stopping patience).

### [Assignment 4: Natural Language Processing & LSTM Emoji Prediction](./assignment_4_lstm_emoji_prediction/)
* **Core Concept:** Engineered a Long Short-Term Memory (LSTM) recurrent neural network in TensorFlow/Keras to predict emojis from unstructured tweet text.
* **Technical Implementation:** Developed a robust NLP text-preprocessing pipeline (regex cleaning, tokenization, sequence padding). Implemented and compared multiple embedding strategies, including random initialization and pre-trained semantic vectors (GloVe-twitter-50D, Gensim FastText).
* **Application & Analysis:** Trained on the `tweet_eval` (emoji) dataset. Conducted cosine similarity matrix evaluations to verify embedding semantic quality. Executed hyperparameter grid searches across epochs and dropout rates, concluding that pre-trained FastText embeddings with moderate dropout (0.2) yielded the highest generalization accuracy.

### [Assignment 5: Naïve Bayes & Decision Tree Classification](./assignment_5_naive_bayes_decision_trees/)
* **Core Concept:** Engineered probabilistic and rule-based classification models for categorical housing data.
* **Technical Implementation:** Hand-calculated prior probabilities and Conditional Probability Tables (CPTs) to implement a Naïve Bayes classifier entirely from scratch, demonstrating a rigorous understanding of Bayes' Theorem. Utilized `scikit-learn` to train a baseline Decision Tree.
* **Application & Analysis:** Extracted explicit `if-then` rules from the Decision Tree structure to analyze model interpretability. Evaluated individual rule coverage fractions and absolute training accuracy to audit the model's decision-making logic.

## Execution & Reproducibility
All projects are formatted as Jupyter Notebooks (`.ipynb`) and are designed to be run sequentially from top to bottom. Datasets required for the classical ML assignments (Assignments 1 and 5) are included in their respective `data/` directories. Deep learning and NLP assignments automatically fetch their datasets via KaggleHub or the Hugging Face `datasets` library.

## Repository Structure
```text
comp5630-machine-learning/
├── assignment_1_linear_regression/
│   ├── data/
│   │   ├── x_train.npy
│   │   ├── y_train.npy
│   │   └── Housing_data_regression.xlsx
│   └── COMP5630_Assignment1.ipynb
├── assignment_2_logistic_regression/
│   └── COMP5630_Assignment2.ipynb
├── assignment_3_cnn_age_regression/
│   └── COMP5630_Assignment3.ipynb
├── assignment_4_lstm_emoji_prediction/
│   └── COMP5630_Assignment4.ipynb
├── assignment_5_naive_bayes_decision_trees/
│   ├── data/
│   │   └── Asssignment5_Data.xlsx
│   └── COMP5630_Assignment5.ipynb
└── README.md
```
---
**Author:** Carter Hand
