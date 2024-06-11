# Heart Failure Prediction using Decision Tree Classifier

This project demonstrates a web application for predicting heart failure using a Decision Tree Classifier. The application is built with Flask and performs hyperparameter tuning using GridSearchCV to find the best parameters for the classifier.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Web Application](#web-application)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project uses a dataset of heart failure clinical records to predict the risk of death due to heart failure. The Decision Tree Classifier is trained with hyperparameter tuning using GridSearchCV to find the optimal model parameters. The web application allows users to input patient data and receive predictions about the risk of heart failure.

## Features

- Hyperparameter tuning using GridSearchCV.
- Training a Decision Tree Classifier with the best parameters.
- Web interface for inputting patient data and receiving predictions.
- JSON response with prediction results.

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/heart-failure-prediction.git
    cd heart-failure-prediction
    ```

2. **Install required packages:**

    ```bash
    pip install -r requirements.txt
    ```

    The `requirements.txt` file should contain:
    ```text
    Flask
    pandas
    scikit-learn
    ```

3. **Download the dataset:**

    Ensure the dataset `heart_failure_clinical_records_dataset.csv` is in the project directory.

## Usage

1. **Run the Flask application:**

    ```bash
    python app.py
    ```

2. **Open your browser and go to:**

    ```
    http://127.0.0.1:5000/
    ```

3. **Input the patient data in the provided form and get the prediction.**

## Dataset

The dataset `heart_failure_clinical_records_dataset.csv` contains clinical records of patients, including features such as age, anaemia, creatinine phosphokinase, diabetes, ejection fraction, platelets, high blood pressure, serum creatinine, serum sodium, sex, smoking, and follow-up period. The target variable is `DEATH_EVENT`, indicating whether the patient died during the follow-up period.

## Model Training

The script uses GridSearchCV to perform hyperparameter tuning for the Decision Tree Classifier. The best parameters are used to initialize and train the classifier. The model is then used to make predictions based on the input data provided through the web application.

## Web Application

The Flask web application allows users to input patient data through a form. The data is then used to make predictions using the trained Decision Tree Classifier. The prediction results are returned as a JSON response and displayed on the web page.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This README file provides an overview of the project, its installation, usage instructions, and other essential details. Make sure to update the repository URL and any specific details as needed.

---

### Example `model.html` file for Flask Application

Create a `templates` folder in your project directory and add a `model.html` file with the following content:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Failure Prediction</title>
</head>
<body>
    <h1>Heart Failure Prediction</h1>
    <form method="post">
        <label for="age">Age:</label>
        <input type="text" id="age" name="age"><br><br>
        <label for="anaemia">Anaemia (0 or 1):</label>
        <input type="text" id="anaemia" name="anaemia"><br><br>
        <label for="creatinine_phosphokinase">Creatinine Phosphokinase:</label>
        <input type="text" id="creatinine_phosphokinase" name="creatinine_phosphokinase"><br><br>
        <label for="diabetes">Diabetes (0 or 1):</label>
        <input type="text" id="diabetes" name="diabetes"><br><br>
        <label for="ejection_fraction">Ejection Fraction:</label>
        <input type="text" id="ejection_fraction" name="ejection_fraction"><br><br>
        <label for="platelets">Platelets:</label>
        <input type="text" id="platelets" name="platelets"><br><br>
        <label for="high_blood_pressure">High Blood Pressure (0 or 1):</label>
        <input type="text" id="high_blood_pressure" name="high_blood_pressure"><br><br>
        <label for="serum_creatinine">Serum Creatinine:</label>
        <input type="text" id="serum_creatinine" name="serum_creatinine"><br><br>
        <label for="serum_sodium">Serum Sodium:</label>
        <input type="text" id="serum_sodium" name="serum_sodium"><br><br>
        <label for="sex">Sex (0 or 1):</label>
        <input type="text" id="sex" name="sex"><br><br>
        <label for="smoking">Smoking (0 or 1):</label>
        <input type="text" id="smoking" name="smoking"><br><br>
        <label for="time">Follow-up period:</label>
        <input type="text" id="time" name="time"><br><br>
        <input type="submit" value="Predict">
    </form>
    <h2>{{ prediction }}</h2>
</body>
</html>
```
