# Emotion-Text-Data-Classification-with-Natural-Language-Processing-NLP-
NLP, Python

Dataset Description

This dataset contains text descriptions expressing various emotions. The emotions included in the dataset are ["joy", "sadness", "anger", "fear", "love", "surprise"]. The dataset is divided into three parts: training data (train.txt), testing data (test.txt), and validation data (val.txt). Each data file consists of text descriptions and their corresponding labels, separated by a semicolon (;).

Problem Statement

The goal of this project is to classify text descriptions into their respective emotions. This is a natural language processing (NLP) text classification problem, specifically a multi-class classification problem.

Approach

Data Understanding

We start by understanding the dataset, which involves exploring its size, checking for null values, and analyzing label distribution. Fortunately, the dataset contains no null values, eliminating the need for data cleaning.

Text Preparation
   
The next step is to prepare the text data for model training. This includes:

Text Tokenization: Breaking down text into individual words or tokens.

One-Hot Encoding: Converting tokens into numerical values using the one_hot library from keras.preprocessing.text.

Padding Sequences: Ensuring that all sequences have the same length by using pad_sequences from Keras.

Model Building

We build a deep learning model for text classification. The model architecture consists of the following layers:

Embedding Layer: Converts the input text into dense vectors.

LSTM Layer: A Long Short-Term Memory layer with 128 units for sequence processing.

Dense Layers: One or more dense layers with a range of parameters.

Output Dense Layer: A dense layer with a softmax activation function and 6 units (equal to the number of emotion classes).

Hyperparameter tuning is performed using RandomSearch from kerastuner to find the best model configuration.

Model Evaluation
The model is evaluated on the test data using metrics from scikit-learn. The evaluation helps us assess the model's performance in classifying emotions in text.

How to Use This Repository

Dataset: Ensure you have access to the dataset, which should include train.txt, test.txt, and val.txt.

Data Preparation: Execute the data_preparation function to preprocess the text data for training and testing.

Model Building: Use the build_model function to create the deep learning model for text classification. Optionally, perform hyperparameter tuning with RandomSearch.

Model Evaluation: Evaluate the model on the test data using metrics provided in the evaluation section.

