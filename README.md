# Cinema Audience Time-Series Forecasting

## Overview

This project focuses on forecasting daily theatre audience attendance across multiple cinema locations using historical audience, booking, and theatre metadata. By leveraging time-series feature engineering and machine learning techniques, the objective is to generate accurate audience predictions that support demand forecasting and operational planning.

---

## Dataset

The analysis combines data from multiple sources:

* `booknow_visits.csv` – Historical daily audience attendance records
* `booknow_booking.csv` – Ticket booking transactions from BookNow
* `booknow_theaters.csv` – Theatre metadata from BookNow
* `cinePOS_booking.csv` – Ticket sales data from cinePOS
* `cinePOS_theaters.csv` – Theatre metadata from cinePOS
* `movie_theater_id_relation.csv` – Mapping between theatre identifiers across platforms
* `date_info.csv` – Calendar information including day-of-week attributes
* `sample_submission.csv` – Submission format for final predictions

---

## Methodology

### 1. Exploratory Data Analysis (EDA)

* Analyzed audience attendance distributions and booking patterns
* Identified outliers, missing values, and data inconsistencies
* Examined weekly and seasonal audience trends
* Explored relationships between bookings, theatre characteristics, and attendance

### 2. Data Preprocessing

* Parsed and standardized date-time features
* Handled missing and duplicate records
* Encoded categorical variables
* Created lag and rolling-window features
* Merged data from multiple sources into a unified dataset

### 3. Feature Engineering

* Combined audience, booking, and theatre information
* Extracted calendar-based features such as weekday and month
* Generated historical attendance statistics
* Created theatre-level and location-specific performance features

### 4. Model Development

The following machine learning models were trained and evaluated:

* Random Forest Regressor
* XGBoost Regressor
* LightGBM Regressor

Models were compared using RMSE, and the best-performing model was selected based on validation performance.

### 5. Forecasting

* Applied the preprocessing pipeline to unseen data
* Generated daily audience forecasts for each theatre
* Exported predictions in the required submission format

---

## Results

### Performance

* **Best Model:** LightGBM Regressor
* **Evaluation Metric:** RMSE (Root Mean Squared Error)
* LightGBM achieved the lowest validation error and the best overall forecasting performance.

### Key Insights

* Weekend screenings consistently attracted larger audiences.
* Theatre characteristics significantly influenced attendance patterns.
* Historical lag features were among the most important predictors.
* Integrating booking data from multiple platforms improved forecast accuracy.

---

## Technology Stack

### Programming Language

* Python

### Libraries & Frameworks

* Pandas
* NumPy
* Scikit-learn
* XGBoost
* LightGBM
* Matplotlib
* Seaborn
* Plotly

---
