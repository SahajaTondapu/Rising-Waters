# Random Forest Model

## Library Imports

The Random Forest model uses the following Python libraries:

- **NumPy** – Used for numerical computations.
- **Scikit-learn** – Provides the `RandomForestClassifier` algorithm and evaluation metrics such as Accuracy Score, Confusion Matrix, and Classification Report.

## Function Definition

A reusable function named `randomForest()` is created to build, train, and evaluate the Random Forest model.

The classifier is initialized with important hyperparameters such as:

- `n_estimators` – Specifies the number of decision trees.
- `random_state` – Ensures reproducible and consistent results.

## Model Training

The model is trained using the `fit()` method.

```python
model.fit(X_train, y_train)
```

During training, the Random Forest algorithm learns patterns from the training dataset by constructing multiple decision trees.

## Prediction

The trained model predicts the output for unseen testing data using the `predict()` method.

```python
y_pred = model.predict(X_test)
```

The predicted values are then compared with the actual test labels to evaluate the model's performance.

## Model Evaluation

The performance of the Random Forest model is evaluated using the following metrics:

### Accuracy Score

- Measures the percentage of correctly predicted observations.
- Provides the overall performance of the model.

### Confusion Matrix

Displays:

- True Positives (TP)
- True Negatives (TN)
- False Positives (FP)
- False Negatives (FN)

It helps evaluate the classification performance in detail.

### Classification Report

The classification report includes:

- **Precision** – Correctly predicted positive observations.
- **Recall** – Correctly identified actual positive observations.
- **F1-Score** – Balance between Precision and Recall.
- **Support** – Number of samples in each class.

## Output

The function prints the evaluation results, including:

- Accuracy Score
- Confusion Matrix
- Classification Report

It also returns:

- The trained Random Forest model.
- Predicted output values for future analysis or deployment.

## Advantages

- High prediction accuracy.
- Reduces overfitting by combining multiple decision trees.
- Handles large datasets efficiently.
- Performs well with both numerical and categorical features.

## Conclusion

The Random Forest algorithm is one of the most reliable ensemble learning techniques for classification tasks. By combining the predictions of multiple decision trees, it improves prediction accuracy, reduces overfitting, and provides robust flood prediction results.
