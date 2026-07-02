# Model Comparison and Selection

## Purpose of `compareModel()`

The `compareModel()` function is used to compare the performance of all trained machine learning models in a single view. It helps identify the best-performing algorithm by evaluating each model using common performance metrics.

## Models Evaluated

The following classification models were trained and tested:

- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)
- XGBoost

## Evaluation Metrics

Each model is evaluated using the following metrics:

### Accuracy Score
- Measures the percentage of correctly classified instances.
- Higher accuracy indicates better model performance.

### Confusion Matrix
- Displays the number of:
  - True Positives (TP)
  - True Negatives (TN)
  - False Positives (FP)
  - False Negatives (FN)
- Helps analyze classification performance in detail.

### Classification Report

The classification report provides:

- **Precision** – Percentage of correctly predicted positive observations.
- **Recall** – Percentage of actual positive observations correctly identified.
- **F1-Score** – Harmonic mean of Precision and Recall.
- **Support** – Number of samples available for each class.

## Model Performance

| Model | Accuracy |
|--------|---------:|
| Decision Tree | 96.55% |
| Random Forest | 96.55% |
| K-Nearest Neighbors (KNN) | Evaluated |
| XGBoost | **96.55%** |

Although Decision Tree, Random Forest, and XGBoost achieved the same accuracy, **XGBoost** was selected as the final deployment model.

## Why XGBoost Was Selected?

- Excellent generalization on structured datasets.
- Boosting algorithm that learns from previous prediction errors.
- More stable than a single Decision Tree.
- Less prone to overfitting.
- Handles complex patterns efficiently.
- Provides reliable prediction performance.

## Deployment

The selected **XGBoost** model is saved using **Pickle** or **Joblib**.

During deployment:

1. The saved model is loaded into the Flask application.
2. User input is preprocessed.
3. The trained XGBoost model generates predictions.
4. The prediction result is displayed to the user.

## References

- Confusion Matrix:
  https://www.analyticsvidhya.com/blog/2020/04/confusion-matrix-machine-learning/

- Classification Report:
  https://medium.com/@kohlishivam5522/understanding-a-classification-report-for-your-machine-learning-model-88815e2ce397

## Conclusion

The model comparison process ensures that the most suitable algorithm is selected based on performance metrics. XGBoost was chosen for deployment because it offers high accuracy, strong generalization, and reliable prediction performance for flood prediction.
