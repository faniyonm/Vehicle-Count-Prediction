# Vehicle-Count-Prediction

## Introduction
Sensors at road junctions collect vehicle count data at different times, helping transport managers make informed decisions. In this project, we aim to predict vehicle counts based on sensor data using machine learning techniques. Vehicle count prediction plays a crucial role in modern intelligent transportation systems by enabling traffic flow monitoring, congestion detection, and forecasting. Accurate predictions not only improve traffic management and urban planning but also enhance road safety and reduce travel delays. Here, we analyze sensor data and build predictive models to estimate vehicle counts, contributing to smarter and data-driven transportation solutions.

## Dataset
The dataset contains two attributes:  
- **Datetime**: Timestamp of data collection  
- **Vehicles**: Number of vehicles at that timestamp  

Since *Vehicles* is numeric, we use a regression approach. A **Random Forest Regressor** is applied, which improves accuracy by averaging predictions from multiple decision trees.

## Feature Extraction
We extract useful features from the **Datetime** column to improve prediction:  
- **Day of the Month** (`get_dom`)  
- **Weekday** (`get_weekday`)  
- **Hour** (`get_hour`)  
- **Year** (`get_year`)  
- **Month**, **Day of Year**, **Week of Year**

The `DateTime` column is converted into proper datetime format, and new columns are created to capture these extracted features.

**Result:**  
The transformed dataset includes these time-based features along with the **Vehicles** column, which records vehicle counts at each timestamp.

## Separate Target Variable
The **Vehicles** column is separated as the target variable, while the remaining features are stored in `train1` for training.

## Model Training
We train a **RandomForestRegressor** using `train1` as features and **Vehicles** as the target variable. Based on the given input features (11, 6, 0, 1, 2015, 11, 2), the model predicts approximately 9 vehicles at that timestamp.

## Conclusion
By extracting meaningful features from the Datetime column and training a Random Forest Regressor, we can effectively predict vehicle counts at given timestamps. This approach supports data-driven solutions for traffic management and intelligent transportation systems.


