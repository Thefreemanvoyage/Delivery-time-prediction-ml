DoorDash Delivery Time Prediction

# Project Overview
Built a machine learning model to predict food delivery times for DoorDash orders using order, restaurant, courier, and weather information available at the time an order is placed.

# Business Problem
DoorDash provides customers with estimated arrival times. Inaccurate delivery estimates can lead to poor customer experiences, refunds, and negative reviews. The objective is to predict delivery time in minutes and identify the key factors that contribute to delivery delays.

# Dataset
Training Dataset -
8,000 delivered orders
March-August 2025
13 columns

Test Dataset -
2,000 held-out orders
Same feature set without target variable

Target Variable -
delivery_minutes

# Exploratory Data Analysis
# Distribution of Delivery Times

<img width="812" height="392" alt="image" src="https://github.com/user-attachments/assets/4ad882ab-2b0b-425c-a65f-26988a34fd67" />

Delivery times are approximately normally distributed with slight right skew.
Mean delivery time: 32.05 minutes.
Distance and restaurant preparation time showed the strongest relationships with delivery duration.
Heavy rain increased delivery times compared with clear weather.
Missing values existed in weather and courier_trips_completed but represented less than 5% of rows.

# Distance vs Delivery Time

<img width="900" height="393" alt="image" src="https://github.com/user-attachments/assets/85307937-680c-445e-9823-2272b0288755" />

# Weather Impact

<img width="912" height="472" alt="image" src="https://github.com/user-attachments/assets/254b5101-fc9e-4cd4-b8be-4a87f1557f00" />

# Feature Importance

<img width="921" height="487" alt="image" src="https://github.com/user-attachments/assets/d58433b6-6db1-4eb7-a20c-5059a36c5981" />


# Feature Engineering

Created additional features -
hour
day_of_week
month
is_weekend
subtotal_per_item
distance_x_prep
The interaction feature distance_x_prep became the most important predictor in the final model.

# Models Evaluated

<img width="1362" height="705" alt="image" src="https://github.com/user-attachments/assets/15700e7b-fb4d-4c5c-82c7-87956126daee" />


# Final Model

Gradient Boosting Regressor achieved the best validation performance.
Validation MAE: 3.36 minutes
This represents approximately a 56% improvement over the baseline model.

# Main Drivers of Delivery Time

Top contributing factors -
Distance × Preparation Time
Restaurant Preparation Time
Courier Vehicle
Hour of Day
Distance
Order Size
Courier Experience
Weather

# Error Analysis

The largest prediction errors occurred in unusually long deliveries, particularly when multiple delay factors occurred simultaneously, such as:

Long travel distances
Slow food preparation
Heavy rain
Large orders

# Deliverables

Trained machine learning model
Feature importance analysis
predictions.csv for 2,000 test orders

# Author
**Rahul B**
rahulsinghb@7338@gmail.com
Bengaluru, India
