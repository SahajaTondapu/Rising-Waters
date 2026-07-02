# Running the Application

## 1. Launching the Application

Follow these steps to start the Flood Prediction System:

1. Open **Anaconda Prompt**.
2. Navigate to the project directory containing the `app.py` file.

```bash
cd path/to/your/project/folder
```

3. Run the Flask application.

```bash
python app.py
```

---

## 2. Accessing the Web Interface

After starting the application, the terminal displays a local server URL similar to:

```text
http://127.0.0.1:5000/
```

Open this URL in your web browser to access the Flood Prediction System.

---

## 3. User Prediction Workflow

1. Open the application home page.
2. Click **Predict Floods**.
3. Enter the required weather parameters such as:
   - Annual Rainfall
   - Seasonal Rainfall
   - Temperature
   - Humidity
   - Cloud Visibility
4. Click the **Submit** button.

---

## 4. Backend Processing

After the user submits the form:

1. The Flask application receives the input values.
2. The saved **StandardScaler** (`transform.save`) standardizes the input data.
3. The saved **XGBoost model** (`floods.save`) predicts the flood status.
4. The prediction result is generated instantly.

---

## 5. Prediction Output

Based on the prediction result, the application redirects the user to one of the following pages:

- **chance.html** – Displays when a flood is predicted.
- **no_chance.html** – Displays when no flood risk is detected.

---

## Workflow Summary

```text
User Input
     │
     ▼
Flask Application (app.py)
     │
     ▼
StandardScaler (transform.save)
     │
     ▼
XGBoost Model (floods.save)
     │
     ▼
Prediction Result
     │
     ├── Flood Risk → chance.html
     └── No Flood Risk → no_chance.html
```

---

## Conclusion

The Flask application integrates the trained machine learning model with a user-friendly web interface. It processes user input, applies the same preprocessing used during training, and generates accurate real-time flood predictions efficiently.
