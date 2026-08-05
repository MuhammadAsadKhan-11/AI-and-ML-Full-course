# 📊 Insurance Charges — Exploratory Data Analysis & Feature Engineering

A complete end-to-end EDA pipeline on a medical insurance dataset, covering data cleaning, encoding, feature engineering, feature scaling, and statistical feature selection (Pearson correlation & Chi-square test).

This project is **Day 1 of a 30-day AI/ML revision series**, where core machine learning concepts are revisited and implemented from scratch through hands-on projects.

---

## 📌 Project Overview

The goal of this project is to explore, clean, and prepare an insurance dataset for downstream machine learning tasks (e.g., predicting insurance charges). Rather than jumping straight into modeling, the focus here is on **doing EDA and preprocessing the right way** — combining visual exploration with statistical hypothesis testing to justify every feature engineering decision.

---

## 📁 Dataset

**File:** `insurance.csv`

| Column   | Description                                  |
|----------|-----------------------------------------------|
| age      | Age of the primary beneficiary                |
| sex      | Gender of the insurance contractor             |
| bmi      | Body Mass Index                                |
| children | Number of children/dependents covered          |
| smoker   | Smoking status                                 |
| region   | Residential area in the US                     |
| charges  | Individual medical costs billed (target)       |

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** – data manipulation
- **NumPy** – numerical operations
- **Matplotlib / Seaborn** – data visualization
- **Scikit-learn** – feature scaling (`StandardScaler`)
- **SciPy** – statistical testing (`pearsonr`, `chi2_contingency`)
- **Jupyter Notebook**

---

## ⚙️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/MuhammadAsadKhan-11/<repo-name>.git
cd <repo-name>

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# Install dependencies
pip install pandas numpy seaborn matplotlib scikit-learn scipy jupyter
```

## ▶️ Usage

```bash
jupyter notebook EDA.ipynb
```

Run the cells sequentially — the notebook is structured to flow from raw data exploration to a final, model-ready dataset.

---

## 🔍 Methodology

### 1. Exploratory Data Analysis
- Inspected dataset shape, structure, and data types (`.shape`, `.info()`, `.describe()`)
- Checked for missing values (`.isnull().sum()`)

### 2. Data Visualization
- **Histograms + KDE** for numeric features (`age`, `bmi`, `children`, `charges`) to study distribution shape
- **Count plots** for categorical features (`sex`, `smoker`, `children`) to check class balance
- **Box plots** to detect outliers in numeric columns

### 3. Correlation Analysis
- Correlation heatmap across numeric features to identify linear relationships and potential multicollinearity

### 4. Data Cleaning
- Removed duplicate records
- Re-validated null values and dataset shape post-cleaning

### 5. Categorical Encoding
- **Binary mapping** for two-class categorical features:
  - `sex` → `is_female` (male: 0, female: 1)
  - `smoker` → `is_smoker` (no: 0, yes: 1)
- **One-hot encoding** (`pd.get_dummies`, `drop_first=True`) for the multi-class `region` column to avoid the dummy variable trap

### 6. Feature Engineering
- Engineered a new categorical feature, `bmi_category`, by binning continuous BMI values into clinically standard ranges:
  - Underweight (< 18.5)
  - Normal (18.5 – 24.9)
  - Overweight (25 – 29.9)
  - Obese (30+)
- One-hot encoded the newly created `bmi_category` feature

### 7. Feature Scaling
- Standardized numeric columns (`age`, `bmi`, `children`) using `StandardScaler` to center them at mean 0 with unit variance

### 8. Statistical Feature Selection
- **Pearson correlation test** (`scipy.stats.pearsonr`) between each numeric feature and `charges`, ranked by absolute correlation strength and significance (p-value)
- **Chi-square test of independence** (`chi2_contingency`) between categorical features and a binned target variable (`charges` split into quartiles via `pd.qcut`), validated against a critical value at **α = 0.05** to statistically confirm which categorical features significantly influence charges

### 9. Final Feature Set
Combined the results of both statistical tests to arrive at a final, reduced feature set:

```
['age', 'is_female', 'bmi', 'children', 'is_smoker', 'charges',
 'region_southeast', 'bmi_category_obese']
```

---

## 📈 Key Takeaways

- Visual EDA (histograms, box plots, heatmaps) is essential for building intuition, but it isn't sufficient on its own for feature selection.
- Pairing visualizations with **statistical hypothesis testing** (Pearson correlation, Chi-square) gives objective, defensible evidence for which features to keep before modeling.
- Feature engineering (like binning BMI into clinical categories) can surface signal that raw numeric values alone may not capture as clearly for a model.

---

## 📂 Project Structure

```
├── EDA.ipynb          # Main notebook: EDA, cleaning, encoding, FE, scaling, feature selection
├── insurance.csv       # Raw dataset
└── README.md           # Project documentation
```

---

## 🚀 Next Steps

- Train baseline regression models (Linear Regression, Random Forest, XGBoost) on the final feature set
- Perform hyperparameter tuning and cross-validation
- Compare model performance using RMSE / R² metrics

---

## 🙋‍♂️ Author

**Muhammad Asad Khan**
Final Year BSSE Student, NUML Islamabad
🔗 [GitHub](https://github.com/MuhammadAsadKhan-11)

Part of a 30-day AI/ML revision series — follow along on [LinkedIn](www.linkedin.com/in/muhammad-asad-khan-9a70243a3) for daily updates.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
