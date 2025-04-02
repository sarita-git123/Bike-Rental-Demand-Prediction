# Bike Rental Demand Prediction - Case Study

## 🚲 Overview
This project analyzes a bike-sharing system dataset to build a predictive model for bike rental demand. The case study focuses on BoomBikes, a US bike-sharing provider that experienced revenue declines during the COVID-19 pandemic and wants to understand factors affecting bike demand to prepare for post-pandemic recovery.

## 📊 Problem Statement
Build a multiple linear regression model to predict the demand for shared bikes based on various features including:

-> Temporal features (season, year, month, holiday, weekday)
-> Weather conditions (temperature, humidity, windspeed, weather situation)
-> Operational features (working day, casual vs registered users)

## 🔍 Business Objectives
1. Identify which variables are most significant in predicting bike demand
2. Understand how these variables describe bike rental patterns
3. Help management develop data-driven business strategies
4. Provide insights for expanding into new markets

## 📂 Dataset
* The dataset contains daily bike rental information with the following key features:
* Temporal Features: season, yr, mnth, holiday, weekday, workingday
* Weather Features: weathersit, temp, atemp, hum, windspeed
* Usage Features: casual, registered, cnt (total rentals = casual + registered)

## 🛠️ Technical Approach
### Data Exploration & Cleaning:
Removed irrelevant columns (instant, dteday, casual, registered)
Created dummy variables for categorical features
Analyzed distributions and correlations
### Feature Engineering:
Created derived features where appropriate
Handled multicollinearity
Normalized/scaled features as needed
### Model Development:
Implemented multiple linear regression
Evaluated using R-squared and other metrics
Performed feature selection to identify key predictors
### Model Evaluation:
Tested assumptions of linear regression
Analyzed residuals
Validated model performance

## 📈 Key Findings
1. **Temperature (`temp`)**  
   - **Coefficient**: +0.4620  
   - **Impact**: A 1-unit increase in temperature increases bike rentals by **0.462 units**.  
   - **Interpretation**: Warmer weather drives higher demand, likely due to comfort and outdoor activity preferences.
  
2. **Weather Situation 3 (`weathersit_3`)**  
   - **Coefficient**: -0.0669 (vs. clear weather, `weathersit1`)  
   - **Impact**: Severe weather (e.g., heavy rain/snow) decreases rentals by **0.0669 units**.  
   - **Interpretation**: Adverse weather conditions reduce demand but have a smaller effect than temperature or yearly trends.

3. **Year (`yr1`)**  
   - **Coefficient**: +0.2213  
   - **Impact**: Year-over-year growth increases rentals by **0.2213 units**.  
   - **Interpretation**: Demand grows consistently annually, reflecting brand growth or market adoption.

### Magnitude of Influence (Descending Order):
1. Temperature (strongest) → 2. Year → 3. Weather Situation 3 (weakest).

## 💡 Business Recommendations
### Operational Adjustments
- **Leverage Weather Trends**:  
  - **High Temp Days**: Increase bike availability, staff, and run promotions (e.g., "Summer Ride Discounts").  
  - **Adverse Weather Days**: Use downtime for maintenance or offer "rainy day" loyalty rewards.  

- **Scale for Growth**:  
  - Expand fleets, docking stations, and service areas **yearly** to match rising demand.  
  - Use predictive analytics to forecast growth and optimize resource allocation.  

### Pricing & Promotions
- **Dynamic Pricing**:  
  - Raise prices slightly on warm days; offer discounts during bad weather.  
- **Membership Drives**:  
  - Promote annual subscriptions to align with yearly growth trends.  

### Customer Experience
- **Weather-Resistant Features**:  
  - Provide bikes with mudguards, better brakes, or partner with brands for rain gear.  
- **Real-Time Weather Alerts**:  
  - Integrate weather alerts in apps, suggesting flexible rentals during storms.  

### Long-Term Strategy
- **Climate Adaptation**:  
  - Monitor climate trends to anticipate demand shifts (e.g., longer summers).  
  - Advocate for shaded bike lanes or covered stations in city planning.  


## 🛠️ Technologies Used
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Statsmodels
