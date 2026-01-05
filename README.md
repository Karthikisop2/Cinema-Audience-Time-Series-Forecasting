# Cinema Audience Time-Series Forecasting

## Overview
This project addresses predicting daily theatre audience counts across multiple locations using historical booking and theatre metadata. Machine learning models are applied to forecast audience numbers accurately.

## Dataset
Multiple CSVs including:
- `booknow_visits.csv` – daily audience counts
- `booknow_booking.csv` – BookNow ticket bookings
- `booknow_theaters.csv` – BookNow theatre metadata
- `cinePOS_booking.csv` – cinePOS ticket sales
- `cinePOS_theaters.csv` – cinePOS theatre metadata
- `movie_theater_id_relation.csv` – mapping between theatre IDs
- `date_info.csv` – day-of-week info
- `sample_submission.csv` – submission template

## Steps
1. **EDA** – audience distributions, outliers, weekday/seasonal trends.
2. **Preprocessing** – datetime parsing, missing values, encoding categorical features, lag & rolling features.
3. **Feature Engineering** – combine bookings, theatre metadata, and time-based features.
4. **Modeling** – RandomForest, XGBoost, LightGBM; compared RMSE, selected best model.
5. **Prediction** – applied preprocessing on test set, predicted audience counts, saved submission.

## Results
- **Key metrics:** LightGBM achieved the best RMSE on validation data.  
- **Insights:** Weekend shows and theatre type strongly affect audience counts; lag features improve predictions.

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn, Plotly.  
