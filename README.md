# IMDB Movie Revenue Prediction

This project aims to predict the financial success of movies based on various features such as budget, genre, and runtime using machine learning techniques. It analyzes a dataset of 1000 movies from IMDB and applies data preprocessing, feature transformation, and predictive modeling.

## 📌 Project Overview

The project involves:
- Data preprocessing and feature engineering
- Exploratory Data Analysis (EDA)
- Application of machine learning models (Random Forest, Support Vector Machines, and Linear Regression)
- Model evaluation using multiple performance metrics

## 📊 Dataset

The dataset used in this project contains information on 1000 movies from **IMDB (2006-2016)**, including:
- **Title**: Movie title
- **Genre**: Movie genres
- **Director**: Director's name
- **Actors**: List of main actors
- **Year**: Release year
- **Runtime**: Movie duration (minutes)
- **Rating**: IMDB rating
- **Votes**: Total votes received
- **Revenue**: Box office earnings (millions)
- **Metascore**: Aggregated critic scores from Metacritic

## 🔍 Data Preprocessing

The dataset was cleaned and transformed before training models:
1. **Handling Missing Data**: 
   - Numerical values were imputed with the median.
   - Categorical values were replaced with a generic "missing" label.
2. **Feature Scaling**:
   - Standardization was applied to numerical features.
3. **Encoding Categorical Variables**:
   - One-hot encoding was used to convert categorical features into numerical representations.

## 🤖 Machine Learning Models

The following models were implemented and evaluated:

### 1️⃣ **Random Forest**
- A tree-based ensemble method that improves prediction accuracy.
- Key hyperparameters tuned:
  - `n_estimators`: 100, 200, 300
  - `max_depth`: 10, 20, 30
  - `min_samples_split`: 2, 5, 10

### 2️⃣ **Support Vector Machine (SVM)**
- Effective for high-dimensional data classification.
- Key hyperparameters:
  - `C`: Regularization parameter
  - `gamma`: Kernel coefficient
  - `kernel`: `rbf`, `poly`, `sigmoid`

### 3️⃣ **Linear Regression**
- Used for predicting continuous values by modeling relationships between variables.

## 📈 Model Performance

The models were evaluated using **Mean Absolute Error (MAE)**, **Mean Squared Error (MSE)**, **Root Mean Squared Error (RMSE)**, **Mean Absolute Percentage Error (MAPE)**, and **R² Score**.

| Model              | MAE  | MSE   | RMSE  | MAPE   | R² Score |
|-------------------|------|------|------|--------|---------|
| **Random Forest** | 38.74 | 4534.27 | 67.34 | 9204.95% | 0.5569 |
| **SVM**          | 39.43 | 4677.01 | 68.39 | 8770.11% | 0.5429 |
| **Linear Regression** | 38.74 | 3442.97 | 58.68 | 14966.44% | 0.6635 |

## 🏆 Key Findings
- **Linear Regression** had the highest R² score (0.6635), indicating better explanatory power.
- **Random Forest** provided a balance between accuracy and interpretability.
- **SVM** performed comparably but struggled with large deviations in predictions.
- The dataset's variability and possible missing data could affect prediction accuracy.


