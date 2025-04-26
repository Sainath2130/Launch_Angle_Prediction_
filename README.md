# Launch_Angle_Prediction_
Predicts the launch angle of a baseball hit using a pre-trained KNN model.
Features
Launch Angle Prediction: Predicts the launch angle of a baseball hit using a pre-trained KNN model.

Interactive Input: Users can enter exit velocity and hit distance through a user-friendly web interface.

Visual Output: Displays a scatter plot visualizing the relationship between exit velocity and launch angle.

Comparison Table: Provides a table comparing the predicted launch angle with other scenarios.

How It Works
Import Libraries:

os: For interacting with the operating system (e.g., file path manipulation).

streamlit as st: For creating the web application.

pickle: For loading the pre-trained KNN (K-Nearest Neighbors) model.

numpy as np: For numerical operations, especially creating arrays for model input.

matplotlib.pyplot as plt: For creating plots to visualize the prediction.

pandas as pd: For creating and displaying dataframes.

Load the KNN Model:

The script loads a pre-trained KNN model (knn_model.pkl) from the models directory.

It handles potential errors during model loading, such as the file not being found or other exceptions.

Create Streamlit App:

The script uses Streamlit to create the web application interface.

Create Sidebar for Input:

The application includes a sidebar with input fields for:

Exit Velocity (mph)

Hit Distance (ft)

A button in the sidebar triggers the launch angle prediction.

Prediction Logic:

When the user clicks the "Predict Launch Angle" button, the application:

Retrieves the entered exit velocity and hit distance.

Prepares the input data for the KNN model.

Uses the loaded KNN model (model.predict()) to predict the launch angle.

Displays the predicted launch angle.

Visualization:

The application generates a scatter plot showing the predicted launch angle in relation to exit velocity.

Comparison Table:

The application calculates and displays a table comparing the user's input with other exit velocity and hit distance values, showing the corresponding launch angles.

Prerequisites
Python 3.x

The following Python libraries:

streamlit

pickle

numpy

matplotlib

pandas

Installation
Clone this repository.

Ensure you have the required Python libraries installed. You can install them using pip:

pip install streamlit pickle numpy matplotlib pandas

Place the pre-trained KNN model file (knn_model.pkl) in the models directory.

Usage
Run the Streamlit application:

streamlit run your_script_name.py  # Replace your_script_name.py

Open the application in your web browser.

Use the sidebar to input the exit velocity and hit distance.

Click the "Predict Launch Angle" button.

View the predicted launch angle, the visualization, and the comparison table.
