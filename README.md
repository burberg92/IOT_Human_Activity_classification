# IOT_Human_Activity_classification

## Introduction
Human Activity Recognition (HAR) is the task of predicting a person's physical activity using data collected from wearable devices' sensors. In this project, our objective is to predict user activities based on accelerometer and gyroscope measurements from smartphones. This entails a multi-class classification problem with twelve possible activity classes:

 - WALKING
 - WALKING UPSTAIRS
 - WALKING DOWNSTAIRS
 - SITTING
 - STANDING
 - LAYING
 - STAND_TO_SIT
 - SIT_TO_STAND
 - SIT_TO_LIE
 - LIE_TO_SIT
 - STAND_TO_LIE
 - LIE_TO_STAND

The dataset provided includes time-series data from the accelerometer and gyroscope sensors, as well as derived features like jerk signals and Fourier-transformed frequency domain signals. The raw sensor data has been pre-processed to eliminate noise and separate acceleration signals into gravitational and body motion components.

Our goal is to develop a machine learning model capable of accurately classifying user activities using these sensor measurements. We will employ the training dataset to train the model and evaluate its performance on the testing dataset. The project's overarching objective is to produce a model applicable in real-world scenarios, particularly in healthcare and fitness tracking, to monitor and enhance human activity recognition for improved patient outcomes and healthy lifestyle promotion.

## Part One
### RNN Model1
In RNN Model1, we focus on constructing a recurrent neural network (RNN) model to categorize user activities into three primary classes:

 - WALKING
 - WALKING UPSTAIRS
 - WALKING DOWNSTAIRS
 - SITTING
 - STANDING
 - LAYING
 - POS (Postural transitions): STAND_TO_SIT, SIT_TO_STAND, SIT_TO_LIE, LIE_TO_SIT, STAND_TO_LIE, and LIE_TO_STAND
   
We employ the datasets X_train, y_train, X_test, and y_test for this purpose.

### RNN Model2
RNN Model2 focuses on creating another recurrent neural network (RNN) model to classify user activities into three main categories:

1. MOT (Movement on foot): WALKING, WALKING UPSTAIRS, and WALKING DOWNSTAIRS
2. SIT (Sedentary inactivity): SITTING, STANDING, and LAYING
3. POS (Postural transitions): STAND_TO_SIT, SIT_TO_STAND, SIT_TO_LIE, LIE_TO_SIT, STAND_TO_LIE, and LIE_TO_STAND

We utilize the datasets X_train, y_train, X_test, and y_test for this purpose.

## Part Two

The second part of the project involves constructing a time series dataframe by aggregating accelerometer (Acc) and gyroscope (Gyro) signals from separate files. This aggregation entails collecting readings at fixed time intervals, creating data points that represent the sensor values at specific time instances. The time series dataframe is formed by concatenating these data points along the time axis to form sequences representing user activity.

Once the time series dataframe is constructed, it is utilized to train a Long Short-Term Memory (LSTM) model. This LSTM model is trained to classify activities into six classes:

 - WALKING
 - WALKING UPSTAIRS
 - WALKING DOWNSTAIRS
 - SITTING
 - STANDING
 - LAYING
 - POS (Postural transitions): STAND_TO_SIT, SIT_TO_STAND, SIT_TO_LIE, LIE_TO_SIT, STAND_TO_LIE, and LIE_TO_STAND

We use data files from the RawData folder, specifically acc_expXX_userYY and gyro_expXX_userYY files.

Feel free to explore the project's components and adapt the models for your own use cases and research goals.
