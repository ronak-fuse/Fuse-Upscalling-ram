# Fuse-Upscalling
# Exploratory Data Analysis (EDA) on Titanic Dataset

## 1. Introduction to EDA
- **EDA (Exploratory Data Analysis)** is the process of using statistical summaries and visualizations to understand dataset characteristics.  
- **Main purposes:**
  - Generate hypotheses  
  - Detect anomalies  
  - Understand relationships between variables  
  - Ensure data quality  
  - Guide model selection  

---

## 2. EDA Process
1. Understand the data and problem  
2. Inspect and prepare the data (size, shape, data types, missing values)  
3. Visualize the data (univariate, bivariate, multivariate)  
4. Perform statistical analysis (descriptive statistics, correlations)  

---

## 3. Dataset Overview
- **Dataset:** Titanic dataset  
- **Shape:** 891 rows × 12 columns  
- **Target variable:** `Survived` (0 = No, 1 = Yes)  
- **Features:**
  - **Numerical:** `Age`, `Fare`, `SibSp`, `Parch`  
  - **Categorical:** `Sex`, `Embarked`, `Pclass`  
  - **High-cardinality:** `Name`, `Ticket`, `Cabin`  

---

## 4. Handling Missing Values
- `Age` → 19.87% missing → Filled with **median**  
- `Embarked` → 0.22% missing → Filled with **mode (‘S’)**  
- `Cabin` → 77.1% missing → **Dropped**  

---

## 5. Data Visualization
- **Univariate:** Histogram, Bar chart, Box plot  
- **Bivariate/Multivariate:** Scatter plot, Heatmap (correlation matrix)  

---

## 6. Feature Encoding
- `Sex` → **Label Encoding** (binary)  
- `Embarked` → **One-Hot Encoding**  
- `Pclass` → Treated as **ordinal numeric**  
- Dropped: `Name`, `Ticket`, `PassengerId` (not useful for modeling)  

---

## 7. Scaling Numerical Features
- Applied **StandardScaler** to:  
  - `Age`, `Fare`, `SibSp`, `Parch`  
- Result: Mean = 0, Std = 1  
- Reason: Prepares data for ML models sensitive to scale  

---

## 8. Statistical & Correlation Analysis
- **Descriptive statistics** used to summarize continuous features  
- **Key correlations:**  
  - `Pclass` ↔ `Fare` (strong negative correlation)  
  - `Sex` ↔ `Survived` (important predictor)  
  - `SibSp` ↔ `Parch` (moderate correlation – family groups)  

---

## 9. Final Cleaned Dataset
- No missing values  
- Encoded categorical variables  
- Scaled numerical variables  
- Dropped irrelevant features  
- **Dataset is ready for Machine Learning modeling**  

---
 Contributed by Ronak Krishna Shrestha 🚀
