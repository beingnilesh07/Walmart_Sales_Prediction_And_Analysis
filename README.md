# 🛒 Walmart Sales Predict & Analysis

<b>Designed and implemented a machine learning pipeline to predict Walmart sales, leveraging advanced data analysis to optimize inventory management and strengthen business strategy.</b>  


##  Problem Statement

Walmart operates thousands of stores across multiple departments, each with fluctuating weekly sales influenced by holidays, promotions, economic conditions, and store characteristics. Inaccurate forecasts lead to overstocking, understocking, and missed revenue opportunities.

This project builds a weekly sales prediction modelthat helps Walmart optimise inventory management, promotional planning, and business strategy with particular focus on how holidays and markdown events drive sales spikes.

---

##  Business Objectives
The main objective of this project is to predict weekly store sales by analyzing how different factors influence sales performance. This includes studying the impact of calendar-related factors such as weeks, months, and holidays, as well as space-based factors like store and department characteristics. Special emphasis is placed on understanding how the presence of holidays within a week affects sales volume, helping identify patterns that drive higher store revenue and improve data-driven decision-making.

##  Technologies Used
- Python  
- SQL  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebooks  

---

##  Dataset Information
The dataset is sourced from **Kaggle** and consists of three CSV files:

- **train.csv** – 115,064 rows  
  - Attributes: `Store`, `Dept`, `Date`, `Weekly_Sales`, `IsHoliday`  

- **stores.csv** – 45 rows  
  - Attributes: `Store`, `Type`, `Size`  

- **features.csv** – 8,190 rows  
  - Attributes: `Store`, `Date`, `Temperature`, `Fuel_Price`, `MarkDown1–5`, `CPI`, `Unemployment`, `IsHoliday`  

---

##  Objective
- Understand and clean the dataset (handling missing values, feature engineering).  
- Build regression models to predict **weekly sales** using single and multiple features.  
- Evaluate and compare models using metrics such as **R²**, **RMSE**, and **MAE**.  
- Provide insights for **business strategy and inventory management**.  

---

## Machine Learning Models Implemented
- **Linear Regression** – baseline model for trend analysis.  
- **Random Forest Regression** – ensemble learning for robust predictions.  
- **K Neighbors Regression** – instance-based learning for local patterns.  
- **XGBoost Regression** – gradient boosting for high-performance forecasting.  

---
##  Exploratory Data Analysis

Key findings from EDA:

- **Type A stores** (largest) consistently generate the highest weekly sales
- **Holiday weeks** — especially Thanksgiving and Christmas — show significant sales spikes above average
- **MarkDown1 and MarkDown2** have the strongest positive correlation with sales among all markdown types
- **Store size** is one of the strongest predictors of weekly sales volume
- **CPI and Unemployment** show a mild negative correlation with sales in economically sensitive departments

---

##  Data Preprocessing

- Merged all three CSV files on `Store` and `Date` keys
- Handled missing values in MarkDown columns (filled with 0, representing no active markdown)
- Engineered new time features: `Week`, `Month`, `Year` from `Date`
- Encoded store `Type` using label encoding
- Applied log transformation on `Weekly_Sales` to reduce skewness
- Train-test split: 80% train / 20% test

---

##  Models & Results

Four regression models were trained and evaluated on the held-out test set.

| Model | MAE | MSE | RMSE | R² Score |
|---|---|---|---|---|
| Linear Regression | 0.0300 | 0.003490 | 0.0591 | 92.27% |
| K-Nearest Neighbors | 0.0399 | 0.006331 | 0.0796 | 85.98% |
| XGBoost Regressor | 0.0194 | 0.001185 | 0.0344 | 97.37% |
| **Random Forest Regressor** | **0.0155** | **0.000951** | **0.0308** | **97.89%** |

 **Random Forest Regressor** was selected as the best model — achieving the highest R² of **97.89%** and the lowest RMSE of **0.031** on the test set.

> Note: Metrics are computed on log-transformed Weekly_Sales values.

---

##  Business Insights

1. **Holidays drive disproportionate revenue** — planning inventory 2–3 weeks ahead of major holidays is critical
2. **Store type matters more than location** — Type A stores outperform B and C regardless of regional factors
3. **Markdown promotions boost sales** — MarkDown1 and MarkDown2 events show the strongest positive impact on weekly revenue
4. **Economic indicators matter** — CPI and unemployment show measurable effects on department-level sales

---

##  Future Improvements

- Add a Streamlit dashboard for interactive sales forecasting by store and department
- Integrate time-series models (Prophet, SARIMA) for seasonal trend decomposition
- Build a Power BI / Tableau dashboard for executive-level reporting
- Explore deep learning approaches (LSTM) for long-term sales forecasting

---

##  Results & Insights
- Random Forest and XGBoost models outperform Linear Regression and KNN.  
- Holiday periods and markdowns significantly influence weekly sales.  
- Store size and type are strong predictors of sales volume.  

---
 

---

