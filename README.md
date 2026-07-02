# Saving the Final Model

## Overview

After evaluating all machine learning models, **XGBoost** was selected as the final model because of its high prediction accuracy and reliable performance. Instead of retraining the model every time a prediction is required, the trained model is saved for future use.

## Why Save the Model?

Saving the trained model provides several advantages:

- Eliminates the need to retrain the model.
- Reduces prediction time.
- Ensures consistent prediction results.
- Improves deployment efficiency.

## Saving the Model

The **Joblib** library is used to save the trained machine learning model and the fitted feature scaler.

### Saved Files

| File Name | Purpose |
|-----------|---------|
| `floods.save` | Stores the trained XGBoost model. |
| `transform.save` | Stores the fitted StandardScaler used during preprocessing. |

## Prediction Workflow

During deployment, the prediction process follows these steps:

1. Load the saved **StandardScaler (`transform.save`)**.
2. Standardize the user input using the loaded scaler.
3. Load the trained **XGBoost model (`floods.save`)**.
4. Pass the transformed input to the model.
5. Generate the flood prediction.
6. Display the prediction result to the user.

## Benefits

- Faster predictions.
- Consistent preprocessing.
- No need for retraining.
- Reliable real-time predictions.
- Easy integration with Flask applications.

## Conclusion

Saving both the trained XGBoost model and the fitted StandardScaler ensures that the deployed Flood Prediction System performs predictions efficiently and consistently. This approach improves deployment speed, maintains prediction accuracy, and provides reliable real-time flood prediction results.
