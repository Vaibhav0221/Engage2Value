# Engage2Value – Predicting Customer Purchase Value  

## 📌 Problem Statement  
The goal of this project is to **predict a customer’s purchase value** based on their **multi-session behavior** across digital touchpoints.  

The dataset captures anonymized user interactions such as:  
- Browser types  
- Traffic sources  
- Device details  
- Geographical indicators  

By modeling these patterns, we can estimate the **purchase potential of each user**, helping optimize **marketing and engagement strategies**.  

---

## 📂 Dataset  
- Provided as part of the **Engage2Value competition**.  
- Contains user-level interaction logs with categorical and numerical features.  
- Target variable: **Purchase Value**.  

### 📊 Dataset Shape  
- **Full Training Data:** `(116023, 52)`  
- **Final Test Data:** `(29006, 51)`

---

## 📑 Summary of Notebook  

| Section | Actions Done | Outcome |
|---------|--------------|---------|
| **1. Importing Libraries** | Loaded pandas, sklearn, seaborn, matplotlib, and XGBoost. | Tools set up for data handling, visualization, and modeling. |
| **2. Data Loading** | Imported train (116k × 52) and test (29k × 51) datasets. | Split into features `X` and target `y`. |
| **3. Data Information** | Explored dataset structure, types, and missing values. | Identified 13 numerical and 38 categorical features. |
| **4. Dummy Regressor** | Used mean prediction baseline. | RMSE ≈ 205M (benchmark). |
| **5. Exploratory Data Analysis** | Analyzed correlations and distributions. | Found pageViews, sessions, hits, devices, and channels impact purchases. |
| **6. Data Preprocessing** | Imputed missing values, dropped sparse columns. | Final clean dataset with 12 numerical features. |
| **7. Feature Engineering** | Created date features (day, month, year, weekday, weekend). | Expanded dataset to 16 features. |
| **8. Dataset Splitting** | Train-test split applied (80/20). | Train: 92k rows, Validation: 23k rows. |
| **9. Models** | Trained LR, Random Forest, and Gradient Boosting. | RF performed best among classical models (R² ~0.19). |
| **10. XGBoost** | Hyperparameter tuning for best fit. | Achieved RMSE ≈ 195M, strongest predictive model. |
| **11. Final Prediction & Submission** | Generated predictions on test data (29k rows). | Saved as `submission.csv`. |


