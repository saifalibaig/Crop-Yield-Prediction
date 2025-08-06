# 🌾 Crop Yield Prediction using Machine Learning

## 📌 Project Overview
Agriculture is a key sector in when it comes to our country, and predicting crop production can help optimize **resource allocation, yield forecasting, and policy-making**. In this project, I used historical crop production data to build **predictive models** that estimate crop yield based on features like **State, District, Crop, Season, Area, and Year**.

Accurate crop prediction can help in **agriculture planning, resource optimization, and policy-making**.

---

## 📊 Dataset
- **Source:** [Agriculture Crops Production in India - Kaggle](https://www.kaggle.com/datasets/pyatakov/india-agriculture-crop-production)
- **Rows:** 345,407  
- **Columns:** 10  
- **Target Variable:** `Yield`

### Key Features:
- `State` - Name of the state
- `District` - Name of the district
- `Season` - Season of cultivation
- `Crop` - Type of crop grown
- `Year`- Year of cultivation
- `Area` - Cultivation area (in hectares)
- `Production` - Total crop production 
- `Yield` - `Target Variable`
---

## ✅ Project Workflow
1. **Dataset Overview**
   - Read Dataset
   - Display first 5 rows
   - Shape & Structure
2. **Exploratory Data Analysis (EDA)**
   - Null value analysis
   - Correlation heatmap of numerical features
   - ANOVA test for categorical columns
   - Production distribution analysis
   - Top crops by production
   - District-wise and season-wise crop production
3. **Data Preprocessing**
   - Imputation using SimpleImputer
   - Cardinality Calculation for Categorical Variables
   - One-hot encoding for low-cardinality variables
   - Frequency encoding for high-cardinality variables
4. **Model Development**
   - **Model 1:** Linear Regression (Baseline)
   - **Model 2:** Ridge Regression (with RandomizedSearchCV tuning)
   - **Model 3:** Lasso Regression (with RandomizedSearchCV tuning)
   - **Model 4:** XGBoost Regressor
     - Manual tuning (7 different parameter sets)
     - Hyperparameter tuning using `RandomizedSearchCV`
5. **Model Evaluation**
   - Metrics: `R²`, `RMSE`, `MSE`, `MAE`
   - Actual vs Predicted scatter plots for all models
6. **Feature Importance**
   - Extracted feature importance from XGBoost

---

## 🤖 Models Implemented & Performance
| Model                 | R² Score  | Observations |
|-----------------------|-----------|--------------|
| Linear Regression     | ~0.79    | Baseline |
| Ridge Regression      | ~0.79    | Similar to LR |
| Lasso Regression      | ~0.79    | Similar to Ridge |
| **XGBoost Regressor** | **0.945** | Best performing model |

---

## 📈 Key Visualizations
- Correlation heatmap of numerical features
- Seasonal and state-wise crop production trends
- Top crops by production
- Actual vs Predicted plots for all models
- XGBoost feature importance chart

---

## ✅ Conclusion
- **XGBoost Regressor** was the best-performing model with an R² score of **0.945** and the lowest RMSE.
- Regularization (Lasso/Ridge) did not significantly improve results compared to Linear Regression.
- Top 5 crops by production: **Coconut**, **Sugarcane**, **Rice**, **Wheat**, **Potato**.
- Highest production seen in states: **Kerela**, **Tamil Nadu**, **Karnataka**, **Andhara Pradesh**, **West Bemgal**.
-  Seasonal trend shows crops cultivated whole year leads in overall production while Kharif and Rabi come after it.


---

## 🌍 Real-World Applications
- Assisting **farmers and policymakers** in making informed decisions on crop planning.
- Optimizing **resource allocation** based on expected production.

---

## 🚀 Future Enhancements
- Incorporate **weather and soil data** for better accuracy.
- Deploy the model using **Flask, FastAPI, or Streamlit** for real-time prediction.
- Build a **dashboard for visualization and decision support**.

---
