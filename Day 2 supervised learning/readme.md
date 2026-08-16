# Ford Car Price Prediction — Linear Regression

A regression project that predicts used Ford car prices from real-world listing data (~18,000 rows), 
covering the full ML workflow from exploratory data analysis to model evaluation.

## 📌 Overview

This project explores how vehicle attributes — year, mileage, transmission, engine size, fuel type, 
and model — influence resale price, and builds a Linear Regression model to predict prices on unseen data.

## 🔍 What's Inside

- **Exploratory Data Analysis (EDA)**
  - Price distribution analysis
  - Correlation heatmap of numerical features
  - Boxplots and scatterplots to study relationships between price and categorical/numerical features

- **Feature Engineering**
  - Categorical encoding comparison: **One-Hot Encoding** vs **Label Encoding**
  - Feature scaling using **StandardScaler**

- **Modeling**
  - Linear Regression (scikit-learn)
  - 70/30 train-test split

- **Evaluation**
  - R² Score
  - Adjusted R² Score
  - Comparison of model performance across the two encoding strategies

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

## 📊 Dataset

Ford car listings dataset (`ford.csv`) — includes model, year, price, transmission, mileage, fuel type, 
tax, mpg, and engine size.

## 🚀 Key Takeaway

The choice of categorical encoding method (One-Hot vs Label) has a measurable impact on model performance — 
a reminder that preprocessing decisions matter as much as the algorithm itself.

## 📂 Usage

```bash
git clone <repo-url>
cd <repo-name>
jupyter notebook linear-regression-a.ipynb
```

## 📈 Future Improvements

- Try Ridge/Lasso regression to handle multicollinearity
- Cross-validation for more robust evaluation
- Feature importance analysis
- Hyperparameter tuning
