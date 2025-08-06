# 🌾 Crop Yield Prediction using Machine Learning

## 📌 Project Overview
Agriculture is a key sector in when it comes to our country, and predicting crop production can help optimize **resource allocation, yield forecasting, and policy-making**. In this project, I used historical crop production data to build **predictive models** that estimate crop yield and production based on features like **State, District, Crop, Season, Area, and Year**.

Accurate crop prediction can help in **agriculture planning, resource optimization, and policy-making**.

---

## 📊 Dataset
- **Source:** Kaggle – Agriculture Crops Production in India  
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
1. **Data Cleaning**
   - Checked for missing values
   - Handled null values in categorical & numeric columns using `SimpleImputer`
2. **Exploratory Data Analysis (EDA)**
   - Correlation heatmap of numerical features
   - Production distribution analysis
   - Top crops by production
   - District-wise and season-wise crop production
3. **Feature Engineering**
   - ANOVA test for categorical columns
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
- **XGBoost Regressor** was the best-performing model with an R² score of **0.89** and the lowest RMSE.
- Regularization (Lasso/Ridge) did not significantly outperform Linear Regression.
- **Key features:** Area, State, and Crop type were the most influential.
- Clear seasonal and state-wise patterns were observed in crop production.

---

## 🌍 Real-World Applications
- Agricultural policy-making and resource allocation
- Yield forecasting for supply chain optimization
- Farmer advisory systems for crop planning

---

## 🚀 Future Enhancements
- Include **weather, rainfall, and soil data** for improved accuracy.
- Test advanced models like **LightGBM and CatBoost**.
- Build a **Streamlit/Flask dashboard** for real-time predictions.
- Deploy as an API or integrate with mobile apps for farmers.

---

## 🛠 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/crop-yield-prediction.git
