# Advertising_Sales_Prediction
 A complete data analysis project on advertising sales prediction using Linear Regression. Includes data exploration, outlier detection, visualization, feature engineering, model training, and evaluation.
# Advertising Sales Prediction

## Overview
This project is a simple **Linear Regression** model built to predict sales based on advertising budgets across different media channels: TV, Radio, and Newspaper. It also includes data exploration, outlier detection, scaling, model training, and evaluation.

---

## Table of Contents
1. [Dataset](#dataset)  
2. [Libraries](#libraries)  
3. [Project Steps](#project-steps)  
4. [Results](#results)  
5. [Usage](#usage)  
6. [Author](#author)  

---

## Dataset
- The dataset used is `Advertising.csv`.  
- Columns include:
  - `TV`: Advertising budget for TV.
  - `Radio`: Advertising budget for Radio.
  - `Newspaper`: Advertising budget for Newspaper.
  - `Sales`: Sales generated.
  - `Total`: Total budget (TV + Radio + Newspaper) [added during preprocessing].

---

## Libraries
- `numpy`  
- `pandas`  
- `matplotlib`  
- `seaborn`  
- `scikit-learn` (for `train_test_split`, `StandardScaler`, `LinearRegression`, metrics)

---

## Project Steps

1. **Load Dataset**  
   - Load the CSV file and explore basic information.
   
2. **Data Exploration**  
   - Check data types, null values, duplicates.  
   - Add a new feature: `Total` (sum of all ad budgets).  
   - Visualize data using pairplots and boxplots.

3. **Outlier Detection & Removal**  
   - Identify outliers using the IQR method.  
   - Remove outliers from all relevant columns.

4. **Split Data**  
   - Features (`X`): TV, Radio, Newspaper  
   - Target (`y`): Sales  
   - Split into training (80%) and testing (20%) sets.

5. **Scaling**  
   - Standardize features using `StandardScaler`.

6. **Model Training**  
   - Train a `LinearRegression` model using scaled training data.

7. **Prediction & Evaluation**  
   - Predict sales on test data.  
   - Evaluate performance using:
     - Mean Absolute Error (MAE)  
     - Mean Squared Error (MSE)

8. **Residual Analysis**  
   - Scatter plot of actual vs predicted sales.

---

## Results
- The linear regression model predicts sales based on advertising budgets.  
- Performance metrics will vary depending on the dataset after outlier removal and scaling.

---

## Usage
1. Clone this repository.  
2. Ensure `Advertising.csv` is in the correct path.  
3. Run the Python script:  
   ```bash
   python advertising_sales_prediction.py
