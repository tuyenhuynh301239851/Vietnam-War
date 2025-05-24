Analysis and Model on War based on THOR dataset (Vietname War, US War,..)

This project is a machine learning application designed to predict the outcome of military air missions based on various mission parameters.

* Library: pandas, matplotlib, seaborn, sklearn, numpy

Here are steps I have worked on:

1. Data Preparation & Feature Engineering
Loaded and cleaned historical mission datasets.
Selected relevant features including:
- Mission timing (TIMEONTARGET, TIMEOFFTARGET)
- Altitude, speed, weapon load
- Aircraft type, country, mission function class

2. Handling Categorical and Numerical Data
Applied LabelEncoder to categorical variables such as:
- country_flying_mission
- MFUNC_DESC_CLASS
- VALID_AIRCRAFT_ROOT
Used StandardScaler to normalize numerical features for better model performance.

3. Model Training
Trained a supervised classification model (RandomForest) to learn from labeled mission outcomes.
Evaluated model accuracy and selected the best model based on performance metrics.

4. Prediction System
Built a function predict_new_mission() to take new mission data as input and return a predicted outcome label.
This function performs:
Input formatting
Label encoding
Feature scaling
Prediction using the trained model
Decoding the predicted label to a human-readable result

5. Tested with Realistic Scenarios
Example mission inputs were tested using known aircrafts like the A-37, mission timing, and parameters such as speed and altitude.
Validated that the model could return results like:
- DESTROYED
- RNO WEATHER
- NO BDA
