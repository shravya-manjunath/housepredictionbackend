# House Price Predictor - Backend

## Overview

The **House Price Predictor Backend** is a Flask-based API designed to predict house prices based on various input parameters such as location, square footage, number of bedrooms, etc. This backend handles requests from the frontend, processes the input data, and returns the predicted price using a pre-trained machine learning model.

## Features

- **Flask-based API:** Lightweight and fast web server.
- **Machine Learning Model Integration:** Uses a pre-trained model (e.g., Linear Regression) for predictions.
- **JSON Responses:** Returns house price predictions in JSON format.
- **CORS Enabled:** Allows cross-origin requests from the frontend.

## Technologies Used

- **Python:** The core language for developing the backend API.
- **Flask:** Web framework used for handling HTTP requests.
- **scikit-learn:** Machine learning library for model training and prediction.
- **pickle:** For loading the pre-trained model.
- **pandas/numpy:** For data manipulation and processing.

## Prerequisites

- **Python 3.x** should be installed on your system.
- Install necessary dependencies using `pip`.

## Installation & Setup

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-repository/house-price-predictor-backend.git
    ```

2. **Navigate to the project directory:**
    ```bash
    cd house-price-predictor-backend
    ```

3. **Create a virtual environment (optional but recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

4. **Install required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

    The `requirements.txt` file should include:
    ```
    Flask
    scikit-learn
    pandas
    numpy
    ```
    If you don't have the file, you can create it manually by adding the above dependencies.

5. **Run the Flask server:**
    ```bash
    python server.py
    ```

    By default, the Flask app will run on `http://127.0.0.1:5000`.

## Model Setup

The pre-trained model (`model.pkl`) should be saved in the `models` directory. The machine learning model could be trained separately using data on house prices, and this model is loaded during runtime to make predictions.

The model is loaded in `server.py` using:
```python
import pickle

# Load the model
with open('models/model.pkl', 'rb') as f:
    model = pickle.load(f)
