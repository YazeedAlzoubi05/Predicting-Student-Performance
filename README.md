# 🎓 Student Performance Prediction with Ridge Regression  

## 📌 Project Overview  
This project applies **Ridge Regression** to predict student performance using the `Student_Performance.csv` dataset. The workflow includes data preprocessing, exploratory data analysis (EDA), model training, and evaluation.  

## Steps Implemented  

1. **Data Loading**  
   - Loaded dataset into pandas.  
   - Checked for missing values → none found (so no imputation needed).  

2. **Data Preprocessing**  
   - Encoded categorical feature: *Extracurricular Activities* (Yes/No → 1/0).  

3. **Exploratory Data Analysis (EDA)**  
   - Correlation heatmap to identify relationships between features and target.  
   - Visualizations (scatterplots, bar charts) to explore patterns.  
   - **Insights:** *Previous Scores* and *Hours Studied* are the strongest predictors of performance.  

4. **Train/Test Split**  
   - Split dataset into **80% training (8,000 samples)** and **20% testing (2,000 samples)** using `random_state=42` for reproducibility.  

5. **Standardization**  
   - Standardized numerical features (`Hours Studied`, `Previous Scores`, `Sleep Hours`, `Sample Papers Practiced`) using `StandardScaler`.  
   - **Scaler was fit only on training data, then applied to both train and test sets** to prevent data leakage.  

6. **Modeling with Ridge Regression**  
   - Trained Ridge model with `alpha=1.0`.  
   - Predicted student performance on the test set.  

7. **Model Evaluation**  
   - Evaluated using **Mean Absolute Error (MAE)**.  
   - Ridge MAE: **~1.61** (on a 0–100 scale → very accurate).  

8. **Feature Importance**  
   - Extracted Ridge coefficients to understand feature influence:  
     - **Previous Scores** and **Hours Studied** dominate.  
     - **Sleep Hours**, **Extracurricular Activities**, and **Sample Papers Practiced** have only minor influence.  

## ✅ Results  
- Ridge Regression achieved **MAE ~1.61**, proving the model effectively predicts performance.  
- Strongest predictors: **Previous Scores** & **Hours Studied**.  

## 📂 Repository Structure  
- `Copy_of_Untitled6.ipynb` → Main Jupyter/Colab notebook with full workflow.  
- `Student_Performance.csv` → Dataset used.  
- `README.md` → Project overview (this file).  
