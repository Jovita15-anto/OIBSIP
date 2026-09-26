# 🚗 Car Price Prediction

## 📌 Project Overview

This project predicts the **selling price of a used car** based on various features such as:

- Year
- Kilometers Driven
- Fuel Type
- Seller Type
- Transmission
- Owner Type

Two machine learning models were implemented and compared:

1. Linear Regression
2. Random Forest Regression

The Random Forest model achieved better performance on the test dataset.

---

## 🎯 Objective

The objective of this project is to build a machine learning model that can estimate the selling price of a used car based on its characteristics.

---

## 📂 Dataset

The dataset contains information about used cars and their selling prices.

### Features

| Feature | Description |
|---|---|
| `year` | Manufacturing year of the car |
| `km_driven` | Number of kilometers driven |
| `fuel` | Fuel type |
| `seller_type` | Type of seller |
| `transmission` | Manual or Automatic |
| `owner` | Number/type of previous owners |

### Target

`selling_price` — the selling price of the car.

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked the dataset structure.
3. Identified duplicate rows.
4. Removed duplicate rows.
5. Performed descriptive statistical analysis.
6. Analyzed categorical features.
7. Dropped the `name` column.
8. Converted categorical variables using one-hot encoding.
9. Split the data into training and testing sets.

### Dataset after preprocessing

```
Shape of X: (3577, 13)
Shape of y: (3577,)
```

---

## 📊 Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand the distribution of car prices and the relationship between different features and the selling price.

### 1. Distribution of Selling Price

A histogram was used to visualize the distribution of car selling prices.

The distribution is right-skewed, with most cars having relatively lower selling prices and a smaller number of cars having very high prices.

### 2. Selling Price vs Year

A scatter plot was used to analyze the relationship between the manufacturing year and selling price.

The visualization shows that newer cars generally tend to have higher selling prices.

### 3. Selling Price vs Kilometers Driven

A scatter plot was used to examine the relationship between kilometers driven and selling price.

Cars with lower kilometers driven generally show higher selling prices, although there is considerable variation.

### 4. Selling Price by Fuel Type

A box plot was used to compare selling prices across different fuel types:

- Petrol
- Diesel
- CNG
- LPG
- Electric

### 5. Selling Price by Seller Type

A box plot was used to compare selling prices across different seller types:

- Individual
- Dealer
- Trustmark Dealer

---

---

## 🤖 Model Building

Two regression models were trained to predict the selling price of used cars.

### 1. Linear Regression

Linear Regression was used as the baseline model.

The model was trained using the training dataset and evaluated on the test dataset.

### 2. Random Forest Regression

Random Forest Regression was used to capture non-linear relationships between the car features and selling price.

The model was trained using the same training and testing datasets.

---

---

## 📈 Model Performance

The models were evaluated using three regression metrics:

- **MAE (Mean Absolute Error)** – measures the average absolute difference between actual and predicted prices.
- **RMSE (Root Mean Squared Error)** – measures prediction error while giving more weight to larger errors.
- **R² Score** – indicates how well the model explains the variation in the target variable.

### Performance Comparison

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | ₹213,071.18 | ₹442,304.97 | 0.393 |
| Random Forest | ₹193,601.41 | ₹423,750.33 | 0.443 |

Based on the test-set results, the Random Forest model produced lower MAE and RMSE values and a higher R² score than Linear Regression.

---

---

## 🔍 Feature Importance

Feature importance was analyzed using the trained Random Forest model to understand which features contributed most to the predictions.

| Feature | Importance |
|---|---:|
| `year` | 0.276128 |
| `km_driven` | 0.275607 |
| `transmission_Manual` | 0.255870 |
| `fuel_Diesel` | 0.080052 |
| `fuel_Petrol` | 0.037555 |
| `seller_type_Individual` | 0.034694 |
| `owner_Second Owner` | 0.023139 |
| `owner_Test Drive Car` | 0.008627 |
| `owner_Third Owner` | 0.004689 |
| `seller_type_Trustmark Dealer` | 0.002580 |
| `owner_Fourth & Above Owner` | 0.001026 |
| `fuel_LPG` | 0.000033 |
| `fuel_Electric` | 0.000000 |

The feature-importance analysis shows that `year`, `km_driven`, and `transmission_Manual` had the highest importance values in the Random Forest model.

---

---

## 📊 Actual vs Predicted Prices

The actual selling prices were compared with the prices predicted by the Random Forest model.

The scatter plot shows the relationship between the actual and predicted selling prices.

The dashed diagonal line represents the ideal case where:

```text
Actual Price = Predicted Price
```

---

## 🚗 Example Prediction

The trained Random Forest model was used to predict the selling price of a sample used car.

### Input Details

| Feature | Value |
|---|---|
| Year | 2018 |
| KM Driven | 50,000 |
| Fuel | Petrol |
| Seller Type | Individual |
| Transmission | Manual |
| Owner | First Owner |

### Predicted Selling Price

**₹575,316.48**

This is the price predicted by the trained Random Forest model for the given input features.

---

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical computations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Scikit-learn** – Machine learning
- **Jupyter Notebook** – Development environment

---

## 📁 Project Structure

```text
DataScience-Task-3-Car-Price-Prediction/
│
├── dataset/
│   └── car_data.csv
│
├── Car_Price_Prediction.ipynb
│
└── README.md
```

---

## 📌 Conclusion

This project demonstrates a complete machine learning workflow for predicting used car selling prices.

The workflow included:

- Data cleaning and duplicate removal
- Exploratory Data Analysis
- Feature encoding
- Train-test splitting
- Linear Regression
- Random Forest Regression
- Model evaluation using MAE, RMSE, and R²
- Feature importance analysis
- Prediction of a new car's selling price

The Random Forest model achieved an R² score of **0.443** on the test dataset and was used for the final example prediction.

---

## 👩‍💻 Author

**Anto Jovita**

B.Tech – Artificial Intelligence & Data Science
