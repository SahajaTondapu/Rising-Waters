# Feature Scaling

## Core Concept

Feature scaling is an important data preprocessing step that brings all input features into a similar numerical range. Without feature scaling, machine learning algorithms may assign greater importance to features with larger values, which can reduce model accuracy and performance.

## StandardScaler

The **StandardScaler** from the Scikit-learn library is used to standardize numerical features.

### Formula

\[
z = \frac{x - \mu}{\sigma}
\]

Where:

- **x** = Original value
- **μ** = Mean of the feature
- **σ** = Standard deviation of the feature

After transformation:

- Mean becomes approximately **0**
- Standard deviation becomes approximately **1**

This ensures that all input features contribute equally during model training.

## Application Rules

- Feature scaling is applied **only to the independent variables (X)**.
- The target variable **(y)** is **not scaled** because it represents the output class.

## Workflow

1. Fit the StandardScaler on the training dataset.
2. Transform the training dataset.
3. Use the same scaler to transform the testing dataset.
4. Save the fitted scaler using Joblib or Pickle.
5. During prediction, apply the saved scaler to new user inputs before passing them to the trained model.

## Advantages

- Normalizes numerical features.
- Improves model stability.
- Reduces feature bias.
- Essential for algorithms such as:
  - K-Nearest Neighbors (KNN)
  - Logistic Regression
  - Support Vector Machine (SVM)

## Example Code

```python
from sklearn.preprocessing import StandardScaler

sc = StandardScaler()

X_train = sc.fit_transform(X_train)
X_test = sc.transform(X_test)
```

## Conclusion

Feature scaling standardizes numerical features so that machine learning algorithms can learn efficiently. Saving and reusing the fitted scaler ensures that real-time input data is processed consistently, leading to accurate and reliable flood prediction.
