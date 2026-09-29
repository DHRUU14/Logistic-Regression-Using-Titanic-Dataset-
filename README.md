# Titanic Logistic Regression

## Overview

This project demonstrates a Logistic Regression machine learning model for predicting whether a passenger survived the Titanic disaster.

The project uses the Titanic dataset and follows the complete machine learning workflow, including data preprocessing, feature selection, train-test splitting, model training, prediction, probability estimation, and model evaluation.

## Objective

The main objective of this project is to build a binary classification model that predicts the survival status of Titanic passengers based on passenger-related features.

The target variable is:

- `0` - Not Survived
- `1` - Survived

## Dataset

The project uses the Titanic dataset stored in `train.csv`.

The following features are used for prediction:

- `Pclass` - Passenger class
- `Age` - Passenger age
- `SibSp` - Number of siblings/spouses aboard
- `Parch` - Number of parents/children aboard
- `Fare` - Passenger fare
- `Sex_male` - Encoded gender information
- `Embarked_Q` - Encoded Queenstown embarkation
- `Embarked_S` - Encoded Southampton embarkation

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Machine Learning Model

### Logistic Regression

Logistic Regression is used as the classification algorithm because the target variable contains two possible outcomes:

- Survived
- Not Survived

The model is trained using the training dataset and then used to predict the survival status of passengers in the testing dataset.

## Project Workflow

The project follows these steps:

1. Load the Titanic dataset
2. Explore the dataset
3. Handle missing values
4. Select relevant features
5. Encode categorical variables
6. Separate input features and target variable
7. Split the dataset into training and testing sets
8. Create the Logistic Regression model
9. Train the model using `fit()`
10. Generate predictions using `predict()`
11. Calculate prediction probabilities using `predict_proba()`
12. Evaluate model accuracy
13. Generate a confusion matrix
14. Generate a classification report
15. Test the model with a new passenger

## Train-Test Split

The dataset was divided into:

- Training samples: 712
- Testing samples: 179

The training data is used to train the Logistic Regression model, while the testing data is used to evaluate its performance on unseen data.

## Model Training

The Logistic Regression model is trained using:

```python
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)

After training, the model is used to make predictions:

y_pred = model.predict(X_test)
Prediction Probability

The project also uses predict_proba() to obtain the probability associated with each class.

y_probability = model.predict_proba(X_test)

This provides the probability of:

Not Survived
Survived
Model Evaluation

The model achieved an accuracy of:

81.01%

The project also evaluates the model using:

Accuracy
Confusion Matrix
Precision
Recall
F1-score
Classification Report
New Passenger Prediction

The trained model is also used to predict the survival outcome of a new passenger based on their characteristics.

The prediction includes:

Predicted survival status
Probability of not surviving
Probability of surviving
Confusion Matrix

A confusion matrix is generated to compare the actual survival status with the model's predicted survival status.

from sklearn.metrics import confusion_matrix, ConfusionMatrixDisplay
Classification Report

The classification report provides:

Precision
Recall
F1-score
Support

for both classes:

Not Survived
Survived
Project Structure
Titanic-Logistic-Regression/
│
├── logistic_regression_titanic.ipynb
├── train.csv
└── README.md
How to Run
Clone or download the repository.
Open the project in Visual Studio Code or Jupyter Notebook.
Make sure Python and the required libraries are installed.
Open:
logistic_regression_titanic.ipynb
Select the Python environment/kernel.
Run the notebook cells from top to bottom.
Key Learning Outcomes

Through this project, the following concepts were implemented:

Data preprocessing
Feature selection
Categorical data encoding
Train-test splitting
Binary classification
Logistic Regression
Model training
Model prediction
Prediction probabilities
Accuracy evaluation
Confusion matrix
Classification report
Prediction on new data
Author

Aryan Jagtap

BCA Student
MIT World Peace University

GitHub: Aryan2006-AJ