# Rainfall--Prediction
## Project Objective
The goal of this project is to predict precipitation levels using weather attributes such as temperature, humidity, wind speed, etc., from the Austin weather dataset. The prediction is made using Linear Regression, and the dataset is analyzed to understand how various features influence precipitation.

## Dataset Used
  - austin_weather.csv: This dataset includes daily weather observations recorded in Austin.
  - Target Variable: PrecipitationSumInches
  - Features: TempAvgF, DewPointAvgF, HumidityAvgPercent, VisibilityAvgMiles, WindAvgMPH, etc.

## Approach & Methodology
1. Step 1: Data Loading and Cleaning
     - Loaded the original dataset using pandas.
     - Removed irrelevant columns such as Events, Date, and SeaLevelPressureLowInches.
     - Replaced special symbols:
         'T' (trace amounts) → 0.0
         '-' (missing data) → 0.0
     - Exported the cleaned dataset to a new CSV file (austin_weather_final.csv) for further   processing.
2. Step 2: Data Preprocessing
   - Separated features (X) and target (Y) from the cleaned dataset.
   - Reshaped the Y variable (precipitation) into a 2D array using reshape(-1,1) for model compatibility.
3. Step 3: Model Training
   - Used LinearRegression from sklearn to fit the model on the data.
   - Trained the model with the entire feature set to predict PrecipitationSumInches.

## Analysis & Visualizations
1. Precipitation Trend Over Time
     - A scatter plot was created using matplotlib to visualize precipitation over a time series (days).
     - A particular day (index 798) was highlighted in red to showcase a specific prediction point.
2. Correlation with Weather Attributes
     - Another visualization was done to explore how each attribute correlates with the target variable over time.
     - Subplots were created to compare:
         - Temperature
         - Dew Point
         - Humidity
         - Sea Level Pressure
         - Visibility
         - Wind Speed
       - Red points show data on a specific reference day (index 798).
  ## Key Findings
     - Precipitation tends to correlate visibly with humidity and dew point.
     - Some features like wind speed and pressure show less variation or weaker visual correlation with precipitation.
     - The linear regression model provides a baseline trend understanding, but complex weather patterns may require non-linear models for higher accuracy.
