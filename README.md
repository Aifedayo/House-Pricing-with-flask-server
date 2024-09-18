# House Pricing with Flask Server

## Overview
This project focuses on predicting house prices using machine learning models served through a Flask web application. The goal is to provide a user-friendly interface where users can input relevant house details and get an accurate price prediction based on trained models.

The solution uses a Flask server for the backend, which serves as a machine-learning model to predict house prices. The front end interacts with the server, allowing users to input property features such as location, number of rooms, and other important factors influencing house prices.

## Case Study
In this case study, we explore how machine learning can be used to predict house prices in a real-world scenario. Accurate price prediction is critical for buyers, sellers, and real estate agents. The data for this project was sourced from various publicly available datasets, capturing features like square footage, location, age of the house, and amenities.

The model employed is trained using a dataset containing various house features. The machine learning algorithms used in this project include linear regression, random forest, and other advanced techniques. The dataset was split into training and testing sets to evaluate the model's performance.

Through this case study, we aim to:
- Identify key factors that affect house prices.
- Build a robust predictive model using historical data.
- Provide an accessible API for users to estimate house prices.

## Solution
The solution revolves around a Flask-based API that serves a trained machine-learning model. Here's a breakdown of how the system works:

1. **Data Collection & Preprocessing**: The dataset is cleaned and preprocessed to ensure it's ready for training. This includes handling missing values, feature scaling, and encoding categorical variables.
   
2. **Model Training**: Various machine learning algorithms are trained on the dataset. The model with the best performance is chosen and deployed.

3. **Flask API**: The trained model is integrated into a Flask web application. This API receives user input via HTTP POST requests, processes the input, and returns a predicted price.

4. **Frontend Interaction**: Users can access the application through a simple web interface where they can input details such as location, number of rooms, and other features.

### Features:
- **User Input**: The user provides details of the house they are interested in.
- **Model Prediction**: The Flask server processes the request and uses the trained model to predict the price.
- **Results Display**: The predicted house price is returned to the user in a clean and simple format.

## How to Test

To test the project locally, follow these steps:

### 1. Clone the Repository
```
git clone https://github.com/Aifedayo/House-Pricing-with-flask-server.git
cd House-Pricing-with-flask-server
```

### 2. Set Up a Virtual Environment
It's recommended to create a virtual environment to manage dependencies.
```
python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### 3. Install Dependencies
Install the required Python packages using the `requirements.txt` file.
```
pip install -r requirements.txt
```

### 4. Run the Flask Server
Start the Flask development server.
```
python server.py
```

The server should now be running at `http://127.0.0.1:5000/`. You can visit this URL in your browser to access the web interface and test the model.

### 5. Test the API
You can use tools like `curl` or Postman to send POST requests to the Flask server. For example, using `curl`:
```bash
curl -X POST http://127.0.0.1:5000/predict \
  -H "Content-Type: application/json" \
  -d '{"location": "New York", "rooms": 3, "size": 1500, "year_built": 1999, "bathrooms": 2}'
```

This will return the predicted house price based on the input data.
