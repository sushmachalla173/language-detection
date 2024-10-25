# language detection
## Overview
The primary objective of this project is to develop a machine learning model capable of detecting the language of a given text snippet. The task involves applying different machine learning algorithms to classify the text into its respective language, and evaluating the performance of these models to identify the most effective approach.

## Dataset
The dataset used in this project is a multilingual collection of text samples, with each entry labeled by its corresponding language. The dataset is structured with two main columns:

Text: A sample of text written in one of the supported languages.

Language: The language label corresponding to the text snippet.

## Dataset Characteristics:
Languages: The dataset contains samples in several languages, including English, French, Spanish, Portuguese, Russian, Italian, and others.

Size: The dataset consists of over 10,000 entries, providing a sufficient volume of data for training and testing machine learning models.

## Project Workflow
The project is organized into the following major steps:

### 1. Data Loading and Exploration
Load the Dataset: The dataset is loaded using pandas, and basic exploratory data analysis (EDA) is performed to understand its structure.

Initial Exploration: Key statistics such as the number of rows, columns, and data types are examined. This includes using methods like .head() and .info() to get a quick snapshot of the dataset.

### 2. Data Preprocessing

Text Vectorization: Since machine learning algorithms cannot directly interpret text, the text data is transformed into numerical format using techniques such as

TF-IDF Vectorization: This method converts text into numerical vectors based on word frequency while down-weighting common words.

Splitting the Dataset: The dataset is split into training and testing sets to evaluate the model performance on unseen data.
### 3. Model Training

Several machine learning algorithms are applied to the preprocessed data. Each model is trained and evaluated using the training and test sets:

Multinomial Naive Bayes: A probabilistic model that performs well for text classification tasks, especially when dealing with categorical data.

Logistic Regression: A statistical model that works well for binary and multiclass classification tasks.

Decision Tree Classifier: A non-parametric supervised learning method used for classification, which splits the data based on feature importance.

Random Forest Classifier: An ensemble learning method that improves upon decision trees by averaging multiple trees to reduce overfitting.

### 4. Model Evaluation
The trained models are evaluated using the following metrics:

Accuracy
Accuracy is the primary metric used for evaluating how many language predictions were correct out of the total predictions made by the model.

Confusion Matrix
A confusion matrix is generated to provide a detailed breakdown of the model’s predictions. This matrix compares the true language labels with the predicted labels, offering insights into which languages are commonly misclassified.

A heatmap visualization is created to display the confusion matrix, making it easy to interpret which languages are misclassified more frequently.

Model Comparison
Each model’s performance is compared based on accuracy, and the confusion matrices are used to evaluate where improvements could be made.  Logistic Regression models showed strong performance, while Naive Bayes performed well on specific languages
### 5. Visualizations
Confusion Matrix Heatmap: A heatmap is generated to visualize the confusion matrix, showing how often each language was correctly or incorrectly predicted.

A confusion matrix is used to visualize the performance of the models across all language classes.

Diagonal Elements: The number of correct predictions for each language.

Off-diagonal Elements: The number of misclassifications, helping to identify which languages are commonly confused with one another.


