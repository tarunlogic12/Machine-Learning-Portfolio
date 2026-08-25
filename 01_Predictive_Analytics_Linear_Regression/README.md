 # 🏡 Predictive Analytics & Linear Regression: Boston Housing Analysis

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange.svg)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-green.svg)](https://scikit-learn.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-teal.svg)](https://seaborn.pydata.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

</div>

---

## 📋 Table of Contents
* [1. Project Overview & Business Objective](#-1-project-overview--business-objective)
* [2. Tech Stack & Libraries](#-2-tech-stack--libraries)
* [3. Dataset Description (`BostonHousing.csv`)](#-3-dataset-description-bostonhousingcsv)
* [4. Theoretical Concepts (Part A)](#-4-theoretical-concepts-part-a)
* [5. Practical Implementation & EDA (Part B)](#-5-practical-implementation--eda-part-b)
* [6. Model Evaluation, Regression Equation & Residual Analysis](#-6-model-evaluation-regression-equation--residual-analysis)
* [7. Repository Structure](#-7-repository-structure)

---

## 🎯 1. Project Overview & Business Objective
Welcome to the **Predictive Analytics & Linear Regression** repository! Working in the capacity of a data analyst, this project solves a core real-world business problem: **predicting continuous house prices (`medv`)** based on regional socio-economic factors, crime rates, property taxes, and structural attributes using the classic **Boston Housing Dataset**[cite: 3]. It bridges foundational ML theory with practical predictive data modeling and error diagnostics.

---

## 🛠️ 2. Tech Stack & Libraries
* **Language:** Python 3.x
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Predictive Modeling & Metrics:** Scikit-Learn (`LinearRegression`, `train_test_split`, `mean_absolute_error`, `mean_squared_error`, `r2_score`)
* **Environment:** Google Colab / Jupyter Notebook (`ML_Basics_Linear_Regression.ipynb`)

---

## 📊 3. Dataset Description (`BostonHousing.csv`)
The dataset comprises 506 rows and 14 numerical attributes representing various housing characteristics in Boston suburbs:
* **crim:** Per capita crime rate by town
* **zn:** Proportion of residential land zoned for lots over 25,000 sq.ft.
* **indus:** Proportion of non-retail business acres per town
* **chas:** Charles River dummy variable (= 1 if tract bounds river; 0 otherwise)
* **nox:** Nitric oxides concentration (parts per 10 million)
* **rm:** Average number of rooms per dwelling *(Key Positive Driver)*
* **age:** Proportion of owner-occupied units built prior to 1940
* **dis:** Weighted distances to five Boston employment centers
* **rad:** Index of accessibility to radial highways
* **tax:** Full-value property-tax rate per \$10,000
* **ptratio:** Pupil-teacher ratio by town
* **b:** $1000(\text{Bk} - 0.63)^2$ where $\text{Bk}$ is the proportion of Black residents by town
* **lstat:** % lower status of the population *(Key Inverse Driver)*
* **medv:** Median value of owner-occupied homes in \$1,000s **(Target Variable)**

---

## 💡 4. Theoretical Concepts (Part A)
The accompanying Jupyter notebook covers detailed explanations for the following fundamental machine learning and analytical questions:
* **Q1. Machine Learning & Types:** Supervised, Unsupervised, and Reinforcement Learning with real-world examples.
* **Q2. Supervised Learning:** Detailed difference between continuous value forecasting (**Regression**) and discrete category prediction (**Classification**).
* **Q3. Linear Regression & Equation:** Mathematical formulation ($Y = b_0 + b_1X_1 + \dots + \epsilon$), along with interpretations of intercept ($b_0$) and feature coefficients ($b_i$).
* **Q4. Evaluation Metrics:** Comprehensive breakdowns of **SSE**, **MSE**, **RMSE**, **$R^2$ Score**, and **Adjusted $R^2$**.
* **Q5. ML Workflow:** Step-by-step pipeline from Problem Definition and Data Collection to Preprocessing, EDA, Model Training, and Evaluation.

---

## 📉 5. Practical Implementation & EDA (Part B)
* **Data Exploration (`Q6`):** Successfully executed `.head()`, `.info()`, and `.describe()` confirming zero missing values across all 506 records.
* **Exploratory Data Analysis (`Q7`):** 
  * Generated multi-variable **Pairplots** to track trends and distributions.
  * Computed and plotted the **Correlation Heatmap** to identify feature collinearity and impact on target `medv`.
  * **Key Predictive Insight:** `rm` (rooms) shows a strong positive correlation ($r \approx 0.70$) with house prices, whereas `lstat` (% lower status) shows a strong inverse correlation ($r \approx -0.74$).

---

## 📐 6. Model Evaluation, Regression Equation & Residual Analysis

### Model Performance Metrics (80-20 Train-Test Split):
* **Mean Absolute Error (MAE):** `3.1891`
* **Mean Squared Error (MSE):** `24.2911`
* **Root Mean Squared Error (RMSE):** `4.9286`
* **$R^2$ Score:** `0.6688` *(Model explains ~66.88% of target variance)*
* **Adjusted $R^2$ Score:** `0.6198`

### Linear Regression Equation:
$$\text{medv} = 30.2468 - 0.1131(\text{crim}) + 0.0301(\text{zn}) + 0.0404(\text{indus}) + 2.7844(\text{chas}) - 17.2026(\text{nox}) + 4.4388(\text{rm}) - 0.0063(\text{age}) - 1.4479(\text{dis}) + 0.2624(\text{rad}) - 0.0106(\text{tax}) - 0.9155(\text{ptratio}) + 0.0124(\text{b}) - 0.5086(\text{lstat})$$

### Coefficient Interpretations (Business Value):
* **`rm` (+4.4388):** Each additional room increases median house value by ~$4,438, holding all other features constant.
* **`lstat` (-0.5086):** A 1% increase in the lower-status population corresponds to a ~$508 drop in home value.

### 🔍 Residual Analysis Diagnostics:
* **Residuals vs Predicted Plot:** Evaluated the error variance to check homoscedasticity, showing residuals evenly dispersed around the zero error line.
* **Residual Distribution Plot:** Verified error normality via kernel density estimation on the prediction residuals, validating the underlying assumptions of ordinary least squares linear regression.

---

## 📂 7. Repository Structure
📁 **01_Predictive_Analytics_Linear_Regression/**  
├── 📄 [ML_Basics_Linear_Regression.ipynb](ML_Basics_Linear_Regression.ipynb)  
├── 📊 [BostonHousing.csv](BostonHousing.csv)  
└── 📝 [README.md](README.md)  

* **Author:** Tarun Das  
* **GitHub Profile:** [Tarunlogic12](https://github.com/Tarunlogic12)
