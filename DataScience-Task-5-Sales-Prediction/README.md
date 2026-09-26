# 📊 Sales Prediction using Linear Regression

## 📌 Project Overview

This project predicts product sales based on advertising expenditure across three different media channels:

- 📺 TV
- 📻 Radio
- 📰 Newspaper

A **Linear Regression** machine learning model is trained to understand the relationship between advertising spending and sales.

---

## 🎯 Objective

The objective of this project is to:

- Analyze advertising data.
- Explore relationships between advertising channels and sales.
- Identify correlations between features.
- Build a Linear Regression model.
- Predict sales based on advertising expenditure.
- Evaluate the model using regression metrics.
- Analyze prediction errors using residuals.
- Save and reuse the trained machine learning model.

---

## 📂 Dataset

The dataset used is the **Advertising Dataset**.

It contains **200 records** and the following features:

| Feature | Description |
|---|---|
| TV | Advertising expenditure on TV |
| Radio | Advertising expenditure on Radio |
| Newspaper | Advertising expenditure on Newspaper |
| Sales | Product sales |

The original dataset also contained an unnecessary `Unnamed: 0` column, which was removed during preprocessing.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

## 🔄 Project Workflow

```
Dataset
   ↓
Data Loading
   ↓
Data Inspection
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Pairplot
   ↓
Correlation Analysis
   ↓
Train-Test Split
   ↓
Linear Regression
   ↓
Sales Prediction
   ↓
Model Evaluation
   ↓
Actual vs Predicted Visualization
   ↓
Residual Analysis
   ↓
Model Saving
   ↓
Model Loading & New Prediction
```

## 🔍 Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand the dataset and
identify relationships between advertising expenditure and sales.

The following analyses were performed:

- Dataset shape and structure
- Missing value analysis
- Descriptive statistics
- Pairplot visualization
- Individual scatter plots for each advertising channel

### Pairplot

A pairplot was used to visualize the relationships between:

- TV and Sales
- Radio and Sales
- Newspaper and Sales

### Scatter Plots

Individual scatter plots were created to analyze:

- Sales vs TV advertising
- Sales vs Radio advertising
- Sales vs Newspaper advertising

## 📈 Correlation Analysis

A correlation matrix was calculated to measure the linear relationship between
advertising expenditure and sales.

The correlation values with Sales were:

| Feature | Correlation with Sales |
|---|---:|
| TV | 0.78 |
| Radio | 0.58 |
| Newspaper | 0.23 |

TV advertising showed the strongest linear relationship with Sales in this
dataset, followed by Radio and Newspaper.

A heatmap was also created to visualize the correlations between all numerical
features.

## 🤖 Machine Learning Model

### Linear Regression

Linear Regression was used as the baseline machine learning model to predict
Sales based on advertising expenditure.

The input features were:

- TV
- Radio
- Newspaper

The target variable was:

- Sales

### Train-Test Split

The dataset was divided into 80% training data and 20% testing data.

```
Training features: (160, 3)
Testing features:  (40, 3)

Training target: (160,)
Testing target:  (40,)
```

## 📊 Model Performance

The Linear Regression model was evaluated using three regression metrics:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### Results

| Metric | Score |
|---|---:|
| MAE | 1.4608 |
| RMSE | 1.7816 |
| R² Score | 0.8994 |

The model achieved an **R² score of 0.8994**, indicating that approximately
89.9% of the variation in Sales is explained by the model on the test data.

A lower MAE and RMSE indicate smaller prediction errors.

## 📉 Actual vs Predicted Sales

An Actual vs Predicted Sales scatter plot was created to compare the model's
predictions with the actual Sales values from the test dataset.

The diagonal reference line represents perfect predictions, where:

```
Actual Sales = Predicted Sales
```

## 📊 Residual Analysis

Residuals represent the difference between the actual and predicted Sales
values.

```
Residual = Actual Sales - Predicted Sales
```

## 💾 Model Saving & New Prediction

The trained Linear Regression model was saved using **Joblib** so that it can
be reused without training the model again.

```python
import joblib

joblib.dump(linear_model, "sales_prediction_model.pkl")

loaded_model = joblib.load("sales_prediction_model.pkl")
```

## 📁 Project Structure

```
DataScience-Task-5-Sales-Prediction/
│
├── dataset/
│   └── Advertising.csv
│
├── Sales_Prediction.ipynb
│
├── sales_prediction_model.pkl
│
└── README.md
```
## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## 📝 Conclusion

This project demonstrated the complete machine learning workflow for predicting
sales using advertising expenditure.

The Linear Regression model achieved an R² score of **0.8994** on the test
dataset. The analysis also showed that TV advertising had the strongest linear
relationship with Sales among the three advertising channels.

The trained model was successfully saved and reused to generate predictions
for new advertising expenditure values.

## 👩‍💻 Author

**Anto Jovita**

B.Tech – Artificial Intelligence and Data Science