# Admission Prediction & Model Optimization

A machine learning regression project for predicting graduate admission probability using feature engineering, polynomial regression, Ridge regularization, ensemble models, and hyperparameter tuning.

## 📌 Project Overview

Graduate admission probability can depend on several academic and profile-related factors, including GRE score, TOEFL score, university rating, statement of purpose, letter of recommendation, CGPA, and research experience.

This project establishes a baseline regression model and evaluates multiple feature engineering and machine learning approaches to improve prediction performance.

The workflow covers:

- Data preprocessing
- Exploratory Data Analysis
- Feature engineering
- Baseline model development
- Polynomial feature expansion
- Ridge regularization
- Ensemble regression
- Hyperparameter tuning
- Model comparison
- Performance evaluation

## 🎯 Objectives

- Analyze factors associated with graduate admission probability.
- Prepare the dataset for regression modeling.
- Establish a Linear Regression baseline.
- Create meaningful engineered features.
- Evaluate polynomial regression with Ridge regularization.
- Compare multiple ensemble regression approaches.
- Tune selected models using hyperparameter optimization.
- Measure improvements using multiple regression metrics.

## 📊 Dataset

The project uses a Graduate Admissions dataset containing variables such as:

- GRE Score
- TOEFL Score
- University Rating
- SOP
- LOR
- CGPA
- Research
- Chance of Admit

The target variable is:

```text
Chance of Admit
🔧 Feature Engineering

Several meaningful features were created to represent relationships within the academic profile, including:

Academic test index
Profile strength
Academic profile
Research × University Rating interaction
CGPA × GRE interaction

These engineered features were evaluated alongside the original variables.

🤖 Models Evaluated

The project compares multiple regression approaches:

Linear Regression
Polynomial Ridge Regression
Tuned Polynomial Ridge
Random Forest
Tuned Random Forest
Extra Trees
Tuned Extra Trees
Gradient Boosting
Tuned Gradient Boosting
📈 Model Performance
Model	RMSE	MAE	MAPE	R²
Tuned Polynomial Ridge	0.0677	0.0476	8.44%	0.8224
Polynomial Ridge	0.0679	0.0481	8.54%	0.8213
Baseline Linear Regression	0.0679	0.0480	8.51%	0.8212
Extra Trees + Features	0.0705	0.0492	8.72%	0.8077
Tuned Random Forest + Features	0.0706	0.0497	8.77%	0.8071
Tuned Extra Trees + Features	0.0710	0.0498	8.85%	0.8048
Random Forest + Features	0.0716	0.0501	8.80%	0.8015
Expanded Tuned Gradient Boosting + Features	0.0726	0.0511	9.07%	0.7958
Gradient Boosting + Features	0.0727	0.0498	8.80%	0.7951
Tuned Gradient Boosting + Features	0.0733	0.0507	8.99%	0.7919
🏆 Best Model

Tuned Polynomial Ridge produced the strongest test performance.

Results:

RMSE: 0.0677
MAE: 0.0476
MAPE: 8.44%
R²: 0.8224

Compared with the baseline Linear Regression model:

RMSE improved by 0.34%
MAE improved by 0.82%
MAPE improved by 0.89%
R² increased by 0.15%

The improvement is relatively small because the baseline Linear Regression model was already performing strongly.

🧠 Why Polynomial Ridge?

Polynomial feature expansion allows the model to represent nonlinear relationships between variables.

However, polynomial expansion can increase the number of predictors and lead to larger coefficients. Ridge regularization adds an L2 penalty to help control this effect.

The combination provided the strongest result among the evaluated approaches.

⚠️ Data Considerations

The dataset is cross-sectional rather than genuinely time-indexed.

Therefore, artificial lag or rolling-window features were not created from row order, since doing so could introduce relationships that do not represent real temporal behavior.

🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook / Google Colab
📁 Repository Structure
Admission-Prediction-Model-Optimization/
│
├── Admission Prediction Model Optimization.ipynb
├── README.md
└── .gitignore
