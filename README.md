# Splitting the Dataset into Independent and Dependent Variables

## Core Concept

Splitting the dataset into independent and dependent variables is an important step before training a machine learning model. This process separates the input features from the target variable, enabling the model to learn the relationship between them and make accurate predictions.

## Independent Variables (X)

The **Independent Variables (X)** are the input features used by the machine learning model for prediction.

### Purpose

- Contain useful information required for prediction.
- Represent the input features of the dataset.
- Help the model identify patterns and relationships.
- Only relevant features are selected to improve prediction accuracy.

## Dependent Variable (y)

The **Dependent Variable (y)** is the target variable that the model is trained to predict.

### Purpose

- Represents the output or prediction label.
- Contains one value for each record in the dataset.
- Used as the expected result during model training.

## Creating X and y

The dataset is divided into input and output variables using the following approach:

```python
X = dataset.drop('class', axis=1)
y = dataset['class']
```

- `X` contains all input features.
- `y` contains the target variable (class).

## Importance

Splitting the dataset into **X** and **y** provides several benefits:

- Separates input and output data.
- Prepares the dataset for train-test splitting.
- Improves model training and evaluation.
- Enables the algorithm to learn meaningful patterns.
- Supports accurate flood prediction.

## Conclusion

Separating the dataset into independent variables (**X**) and the dependent variable (**y**) is a fundamental preprocessing step. It ensures that the machine learning model learns from the input features and predicts the correct output efficiently.
