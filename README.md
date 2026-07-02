# Outlier Handling

Outlier handling is an important data preprocessing step because extreme values can negatively affect the performance of machine learning models. Outliers are identified using statistical methods and visualization techniques before model training.

## What are Outliers?

Outliers are data points that significantly differ from the majority of observations in the dataset. These extreme values may occur due to measurement errors, data entry mistakes, or natural variations.

## Detecting Outliers

The following techniques are used to identify outliers:

### Box Plot

- Visualizes the spread of numerical data.
- Helps identify values that lie outside the normal range.
- Clearly displays the median, quartiles, and extreme values.

### Interquartile Range (IQR)

The Interquartile Range (IQR) method detects outliers using the following calculations:

- **IQR = Q3 − Q1**
- **Lower Bound = Q1 − 1.5 × IQR**
- **Upper Bound = Q3 + 1.5 × IQR**

Values outside these bounds are considered outliers.

## Outlier Treatment

Instead of removing outliers, the **IQR-based capping technique** is applied.

- Values greater than the upper bound are replaced with the upper bound.
- Values lower than the lower bound are replaced with the lower bound.

This method preserves the dataset size while minimizing the impact of extreme values.

## Workflow Impact

Handling outliers improves data quality and model performance by:

- Reducing the influence of extreme values.
- Maintaining dataset consistency.
- Preventing biased predictions.
- Improving the accuracy and reliability of machine learning models.
