
# Ride Price Estimation Project

## Project Overview
Build a machine learning system to estimate ride prices using trip and contextual factors. Demonstrates the full ML workflow: data design, cleaning, feature engineering, regression, classification, evaluation, and reflection.

## Dataset Description
- Synthetic dataset with 200 rows.  
- Includes numerical and categorical features.  
- Target variable: `ride_price` (continuous).  
- Simulates realistic trip scenarios with varying distance, duration, demand, traffic, and weather.

## Features and Justification
- **distance_km (numerical):** Longer trips cost more.  
- **trip_duration_min (numerical):** Longer trips may increase price.  
- **time_of_day (categorical):** Peak hours may raise prices.  
- **traffic_level (categorical):** Heavy traffic can increase fare.  
- **weather_condition (categorical):** Bad weather may raise prices.  
- **demand_level (categorical):** High demand triggers surge pricing.  
- **pickup_zone (categorical):** Certain areas (airport, downtown) have higher base fares.  

*Excluded feature:* Passenger age – irrelevant to pricing.

## How to Run
1. Install required packages:  
   ```bash
   pip install pandas numpy scikit-learn matplotlib
Download the dataset: synthetic_ride_price_dataset.csv.

Open the notebook and run all cells.

## Key Findings

Regression predicts continuous prices effectively (MSE, R² metrics).

Classification identifies high-cost rides based on a median price threshold.

Most influential features: distance_km, trip_duration_min, demand_level.

Poor data quality (missing values, outliers, inconsistent labels) can reduce performance.

Ethical considerations: surge pricing may unfairly impact some riders; synthetic data may not cover rare scenarios.
