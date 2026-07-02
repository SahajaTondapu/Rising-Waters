# Decision Tree Model

## Function Initialization

A separate function named `decisiontree()` is created to build, train, and evaluate the Decision Tree model. The function accepts the following parameters:

- `X_train`
- `X_test`
- `y_train`
- `y_test`

This modular approach makes the code reusable, organized, and easy to maintain.

## Algorithm Overview

The **DecisionTreeClassifier** from the Scikit-learn library is used to build the prediction model.

A Decision Tree is a supervised machine learning algorithm used for classification and prediction. It works by splitting the dataset into multiple branches based on feature values.

Each internal node represents a decision condition, while each leaf node represents the final predicted class.

## Model Training

The model is trained using the `fit()` method.

During training, the algorithm learns the relationship between the input features and the target variable.

```python
model.fit(X_train, y_train)
```

## Prediction

After training, the `predict()` method is used to generate predictions on the testing dataset.

```python
y_pred = model.predict(X_test)
```

The predicted values are compared with the actual values to evaluate model performance.

## Model Evaluation

The performance of the Decision Tree model is evaluated using the following metrics:

### Confusion Matrix

The confusion matrix displays:

- True Positives (TP)
- True Negatives (TN)
- False Positives (FP)
- False Negatives (FN)

It helps determine how accurately the model classifies flood predictions.

### Classification Report

The classification report includes:

- **Precision** – Percentage of correctly predicted positive observations.
- **Recall** – Percentage of actual positive observations correctly identified.
- **F1-Score** – Harmonic mean of Precision and Recall.
- **Support** – Number of actual samples available for each class.

## Advantages

- Easy to understand and interpret.
- Handles numerical and categorical data.
- Requires minimal data preprocessing.
- Suitable for classification problems.

## Conclusion

The Decision Tree model is trained and evaluated to determine its prediction performance. If the model achieves satisfactory accuracy, it can be selected for deployment. Otherwise, its performance is compared with other algorithms such as Random Forest, K-Nearest Neighbors (KNN), and XGBoost to identify the best-performing model.
