# 🚢 Task 1: Data Cleaning & Preprocessing (Titanic Dataset)

**Author:** Nandita  
**Program:** Synent Technologies - Data Science Internship  

---

### 📌 Problem Statement
Raw datasets contain missing values, extreme outliers, and incorrect data types. The goal of this task is to clean and preprocess the Titanic dataset to prepare it for Exploratory Data Analysis (EDA) and Machine Learning models.

---

### 📊 Dataset Details
* **Dataset:** Titanic Passenger Dataset (Kaggle)
* **Target Feature:** `Survived`
* **Key Features:** `pclass`, `sex`, `age`, `sibsp`, `parch`, `fare`, `cabin`, `embarked`

---

### ⚙️ Approach
1. **Schema Standardization:** Cleaned column headers to standard `lower_snake_case`.
2. **Missing Data Imputation:** 
   * Filled missing `age` values using group medians based on `pclass` and `sex`.
   * Imputed `embarked` using mode ('S').
   * Transformed missing `cabin` data into a binary flag (`has_cabin`).
3. **Feature Transformation:** Applied log transformation (`np.log1p`) on `fare` to fix right-skewness.
4. **Feature Engineering:** Combined `sibsp` and `parch` to create `family_size`.
5. **Memory Optimization:** Converted text columns into Pandas `category` types.

---

### 💡 Results
* **Accurate Age Estimation:** Group median preserved realistic age variations across passenger classes.
* **Extracted Hidden Signals:** `has_cabin` revealed that passengers with recorded cabins had higher survival rates.
* **Normalized Skewness:** Reduced extreme outlier impact in ticket fares.
* **Family Insights:** Solo travelers showed significantly lower survival rates than small families (2–4 members).
