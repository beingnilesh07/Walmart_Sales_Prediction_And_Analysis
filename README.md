# 🛒 Walmart Sales Predict & Analysis

<b>Designed and implemented a machine learning pipeline to predict Walmart sales, leveraging advanced data analysis to optimize inventory management and strengthen business strategy.</b>  

---
## 🎯 Business Objectives
The main objective of this project is to predict weekly store sales by analyzing how different factors influence sales performance. This includes studying the impact of calendar-related factors such as weeks, months, and holidays, as well as space-based factors like store and department characteristics. Special emphasis is placed on understanding how the presence of holidays within a week affects sales volume, helping identify patterns that drive higher store revenue and improve data-driven decision-making.

## ⚙️ Technologies Used
- Python  
- SQL  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebooks  

---

## 📂 Dataset Information
The dataset is sourced from **Kaggle** and consists of three CSV files:

- **train.csv** – 115,064 rows  
  - Attributes: `Store`, `Dept`, `Date`, `Weekly_Sales`, `IsHoliday`  

- **stores.csv** – 45 rows  
  - Attributes: `Store`, `Type`, `Size`  

- **features.csv** – 8,190 rows  
  - Attributes: `Store`, `Date`, `Temperature`, `Fuel_Price`, `MarkDown1–5`, `CPI`, `Unemployment`, `IsHoliday`  

---

## 🎯 Objective
- Understand and clean the dataset (handling missing values, feature engineering).  
- Build regression models to predict **weekly sales** using single and multiple features.  
- Evaluate and compare models using metrics such as **R²**, **RMSE**, and **MAE**.  
- Provide insights for **business strategy and inventory management**.  

---

## 🧠 Machine Learning Models Implemented
- **Linear Regression** – baseline model for trend analysis.  
- **Random Forest Regression** – ensemble learning for robust predictions.  
- **K Neighbors Regression** – instance-based learning for local patterns.  
- **XGBoost Regression** – gradient boosting for high-performance forecasting.  

---

## 🔄 Workflow
1. **Data Preprocessing**
   - Handle missing values  
   - Feature engineering (holiday flag, markdown features, lag variables)  
   - Encoding categorical variables  
   - Train-test split  

2. **Exploratory Data Analysis (EDA)**
   - Sales distribution across stores and departments  
   - Impact of holidays and markdowns on sales  
   - Correlation analysis of features  

3. **Model Training & Evaluation**
   - Train multiple regression models  
   - Evaluate using R², RMSE, MAE  
   - Compare performance across models  

4. **Visualization**
   - Sales trends over time  
   - Feature importance plots  
   - Residual analysis  

---

## 📊 Evaluation Metrics
- **R² (Coefficient of Determination)** – measures goodness of fit  
- **RMSE (Root Mean Squared Error)** – penalizes large errors
- **MSE (Mean Squarred Erro)** - average of squared prediction errors.
- **MAE (Mean Absolute Error)** – average magnitude of errors  

---

## 🚀 Results & Insights
- Random Forest and XGBoost models outperform Linear Regression and KNN.  
- Holiday periods and markdowns significantly influence weekly sales.  
- Store size and type are strong predictors of sales volume.  

---

## 🤝 Acknowledgements
The dataset is taken from **Kaggle Walmart Sales Forecasting Challenge**.  

---

