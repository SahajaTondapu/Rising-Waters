# Frontend Development

## Overview

The frontend of the Flood Prediction System is developed using the Flask framework. It uses the **templates/** folder to store HTML pages and the **static/** folder to store CSS and JavaScript files. This structure provides a clean, organized, and user-friendly interface for interacting with the flood prediction model.

## templates/ Folder (HTML Pages)

The **templates/** folder contains the HTML pages used by the application.

### home.html

- Landing page of the application.
- Introduces the Flood Prediction System.
- Provides navigation to the prediction page.

### index.html

- Contains the input form for weather parameters.
- Collects user input and sends it to the Flask backend for prediction.

### chance.html

- Displays when the model predicts a **high probability of flooding**.
- Shows an alert message to the user.

### no_chance.html

- Displays when the model predicts **no flood risk**.
- Shows a safe status message.

---

## static/ Folder (Frontend Assets)

The **static/** folder stores the application's styling and interactive files.

### main.css

- Controls the layout and design.
- Improves the appearance of the application.
- Provides responsive styling for different screen sizes.

### main.js

- Adds interactivity to the web pages.
- Performs form validation.
- Handles button actions and client-side functionality.

---

## Folder Structure

```text
Flood_Prediction/
│
├── templates/
│   ├── home.html
│   ├── index.html
│   ├── chance.html
│   └── no_chance.html
│
├── static/
│   ├── main.css
│   └── main.js
│
└── app.py
```

## Advantages

- Well-organized project structure.
- Easy to maintain and update.
- Improves user experience.
- Separates frontend and backend logic.
- Supports scalable web application development.

## References

- HTML: https://www.w3schools.com/html/
- CSS: https://www.w3schools.com/css/
- JavaScript: https://www.w3schools.com/js/

## Conclusion

Separating HTML templates and static assets creates a clean, maintainable, and professional Flask application. This structure improves usability, simplifies development, and provides an effective interface for real-time flood prediction.
