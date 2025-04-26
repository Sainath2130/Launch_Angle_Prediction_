# Launch_Angle_Prediction_
This Python script creates an interactive web application that predicts baseball launch angles based on user-provided exit velocity and hit distance.

### Features

* **Launch Angle Prediction:** Predicts the launch angle of a baseball hit using a pre-trained KNN model.
* **Interactive Input:** Users can enter exit velocity and hit distance through a user-friendly web interface.
* **Visual Output:** Displays a scatter plot visualizing the relationship between exit velocity and launch angle.
* **Comparison Table:** Provides a table comparing the predicted launch angle with other scenarios.

### How It Works

1.  **Import Libraries:**

    * `os`: For interacting with the operating system (e.g., file path manipulation).
    * `streamlit as st`: For creating the web application.
    * `pickle`: For loading the pre-trained KNN (K-Nearest Neighbors) model.
    * `numpy as np`: For numerical operations, especially creating arrays for model input.
    * `matplotlib.pyplot as plt`: For creating plots to visualize the prediction.
    * `pandas as pd`: For creating and displaying dataframes.

2.  **Load the KNN Model:**

    * The script loads a pre-trained KNN model (`knn_model.pkl`) from the `models` directory.
    * It handles potential errors during model loading, such as the file not being found or other exceptions.

3.  **Create Streamlit App:**

    * The script uses Streamlit to create the web application interface.

4.  **Create Sidebar for Input:**

    * The application includes a sidebar with input fields for:
        * Exit Velocity (mph)
        * Hit Distance (ft)
    * A button in the sidebar triggers the launch angle prediction.

5.  **Prediction Logic:**

    * When the user clicks the "Predict Launch Angle" button, the application:
        * Retrieves the entered exit velocity and hit distance.
        * Prepares the input data for the KNN model.
        * Uses the loaded KNN model (`model.predict()`) to predict the launch angle.
        * Displays the predicted launch angle.

6.  **Visualization:**

    * The application generates a scatter plot showing the predicted launch angle in relation to exit velocity.

7.  **Comparison Table:**

    * The application calculates and displays a table comparing the user's input with other exit velocity and hit distance values, showing the corresponding launch angles.

### Prerequisites

* Python 3.x
* The following Python libraries:
    * streamlit
    * pickle
    * numpy
    * matplotlib
    * pandas

### Installation

1.  Clone this repository.
2.  Ensure you have the required Python libraries installed. You can install them using pip:

    ```
    pip install streamlit pickle numpy matplotlib pandas
    ```

3.  Place the pre-trained KNN model file (`knn_model.pkl`) in the `models` directory.

### Usage

1.  Run the Streamlit application:

    ```
    streamlit run your_script_name.py # Replace your_script_name.py
    ```

2.  Open the application in your web browser.
3.  Use the sidebar to input the exit velocity and hit distance.
4.  Click the "Predict Launch Angle" button.
5.  View the predicted launch angle, the visualization, and the comparison table.
