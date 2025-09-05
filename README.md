# GTC ML Project 1 – Data Cleaning & Preprocessing Challenge

## 🏆 Objective

The objective of this project is to build a **robust data preprocessing pipeline** for predicting hotel booking cancellations. The focus is on transforming raw data into a **clean, machine-learning-ready dataset**, ensuring the quality of preprocessing directly supports future model performance. This project does **not include model building**.

---

## 📂 Dataset

The dataset is sourced directly from a Property Management System (PMS) and includes:

- Customer information  
- Booking details  
- Stay specifics  
- Reservation status  

The raw data was uploaded to Kaggle along with the project notebook for reproducibility and exploration.

---

## Phase 1: Exploratory Data Analysis (EDA)

During EDA, the dataset was analyzed to understand:

- **Missing values**: Columns with missing entries were identified and quantified.  
- **Outliers**: Extreme values in key numerical features such as Average Daily Rate (ADR) and lead time were detected and assessed.  
- **Duplicates**: Duplicate rows were found and documented.  
- **Summary statistics**: Distributions, central tendencies, and ranges were reviewed to assess data quality.  

**Key observations from EDA:**

- Several columns contained missing or inconsistent data, including `children`, `country`, and `agent`.  
- Certain numerical columns had significant outliers that could bias model predictions.  
- Duplicate entries were present and needed removal.  
- Data type inconsistencies were noted, particularly in date fields.  

---

## Phase 2: Data Cleaning

The data cleaning phase involved:

- **Handling missing values**: Missing entries were carefully imputed using appropriate strategies, including median or mode replacement and categorical placeholders.  
- **Removing duplicates**: All exact duplicate records were removed to avoid skewed analysis.  
- **Managing outliers**: Extreme values in numerical features were capped to prevent undue influence on model training.  
- **Correcting data types**: Columns were adjusted to appropriate formats to ensure consistency, especially date columns.  

These steps ensured the dataset was consistent, complete, and suitable for processing.

---

## Phase 3: Feature Engineering & Preprocessing

New features were created to enhance the dataset’s predictive power:

- **Total guests**: Combined count of adults, children, and babies.  
- **Total nights**: Sum of weekend and weekday nights.  
- **Family booking flag**: A binary indicator showing whether a booking included children or babies.  

Categorical variables were encoded appropriately, balancing low-cardinality features with standard encoding techniques and grouping high-cardinality features to maintain model efficiency.  

Additionally, columns that could cause **data leakage** were removed, ensuring the resulting dataset reflects information available at the time of booking and is suitable for predictive modeling.

---

## Phase 4: Train/Test Preparation

The cleaned dataset was split into **training and testing sets** to prepare for model development. This split ensures that models trained on this dataset can be reliably evaluated on unseen data.

---

## ✅ Summary

- The dataset has been thoroughly **cleaned** and **preprocessed**.  
- Missing values and duplicates have been addressed, and outliers capped.  
- New features were engineered to enhance predictive performance.  
- Categorical variables were encoded, and data leakage was eliminated.  
- The resulting dataset is **ready for machine learning** tasks related to hotel booking cancellation prediction.  

---

## 📁 Project Structure

