# Kaggle's Bike Sharing Demand
Solving [Kaggle](https://www.kaggle.com/)'s ['Bike Sharing Demand' competition](https://www.kaggle.com/c/bike-sharing-demand) as a final project

for [Naya college](http://www.naya-college.co.il/)'s [Data Science Professional course](http://www.naya-college.co.il/courses/data-scientist-professional/) instructed by Amit Rappel :+1:.

# Summary

## 1. Data Exploration
* Distinguish casual from registered customer by creating many custom graphs and plots:
  - Showing registered vs. casual rentals across day of the week
  - Showing registered vs. casual rentals across hour of the day
  - Showing average users count by weekday & hour of the day across user type
  - Showing registered vs. casual users count by hour of the day across weekdays
  - Showing registered vs. casual rentals by working day
  - Showing registered vs. casual rentals by season
  - Showing average temperatures by season
  - Showing registered vs. casual users count by hour of the day across seasons
  - Showing registered vs. casual rentals by weather
* Histogram the data and different targets
* Correlation analysis of the weather features

## 2. Feature Engineering / Data Manipulation
* Removing outliers from the weather features
* Extracting features from the Datetime column: Year, Month, Quater, Weekday, Hour
* Engineering new features from the Datetime column: isweekend, peak_hour, afternoon
* Engineering a new feature from the weather column: good_weather
* Scaling of 3 weather columns using StandardScaler
* Apply log(x+1) on the target columns - registered & casual counts

## 3. Execution
* Creating 2 different models for registered and casual customers
* Using 2 pipelines with custom transformers:
  - Add custom detail date and weather related columns transformer
  - Standard Scaler Transformer
  - Column Copier Transformer
  - Drop Column Transformer
  - Binned Data Digitizer Transformer
* Trying out many options of different features as input to the 2 models
* Applying RandomForest and XGBoost regressors using GridSearchCV

## 4. Validation
* Defining a RMSLE function and scorer
* Performing Cross Validation

## 5. Using test data for preparing competition submission
