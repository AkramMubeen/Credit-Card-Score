# Credit-Card-Score
# Credit-Card-Offer-Acceptance

## Table of Contents 
1. [Problem Definition](#problem-defintion)
2. [Project Outline](#project-outline)
3. [How to Run the Project](#how-to-run-the-project)

## Problem Definition
This project aims to explore customer acceptance trends of credit card offers from financial institutions. By analyzing this data, the objective is to gain a better understanding of the factors influencing offer acceptances and predict whether a customer is likely to accept or decline the offer. 
Project dataset can be found [here](https://www.kaggle.com/datasets/thedevastator/unlocking-credit-card-offer-acceptance-trends-in)

## Project Outline
The project consists of several components:

Jupyter Notebook: In the Jupyter Notebook, data is cleaned, exploratory data analysis is performed, and various machine learning models are trained and tuned to assess their performance.

Training the Model: The final training occurs in train.py. The best model is selected and saved to a file for future use.

Creating a Flask App: The predict.py script serves as the Flask app, where the saved model is used to predict a customer's decision based on the provided data.

Testing the Service: The request.py script is used for testing the prediction service. It sends a request to the Flask app, which returns the estimated answer based on customer data.

Creating a Dockerfile: A Dockerfile is created to set up a virtual environment using Docker and run the service.

## How to Run The Project
Clone the Repo. Navigate to the directory where you cloned the repository . Once in the project folder, create a virtual environment and activate it using credit-env\Scripts\activate.bat. Install the required libraries from the requirements.txt file by running pip install -r requirements.txt. Optionally, retrain the model by executing the train.py file with the command python train.py. Deploy the Flask app locally by running the predict.py file. It is recommended to use a production server like Waitress (for Windows OS) or Gunicorn (for UNIX). You can run it directly with python predict.py or with Waitress using waitress-serve , or with Gunicorn using gunicorn . The prediction service should now be running locally . Finally, send a POST request to the service using the request.py file or create your own request based on the file's format and run it with python request.py. Alternatively, you can build and run the Dockerfile locally.
