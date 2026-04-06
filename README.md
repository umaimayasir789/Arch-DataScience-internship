# Arch-DataScience-internship
# Data Science Projects

This repository contains two machine learning projects: **Titanic Survival Prediction** and **Stock Price Prediction**. Both projects demonstrate data preprocessing, feature engineering, model building, evaluation, and visualization techniques using Python.

---

## **Project 1: Titanic Survival Prediction**

### **Overview**
The Titanic Survival Prediction project aims to predict whether a passenger survived the Titanic disaster based on historical passenger data. The dataset includes features such as age, sex, passenger class, fare, and more.

### **Dataset**
- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- Format: CSV
- Features:
  - `PassengerId`, `Pclass`, `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Ticket`, `Fare`, `Cabin`, `Embarked`
  - Target: `Survived` (0 = No, 1 = Yes)

### **Steps Performed**
1. **Data Preprocessing**
   - Handle missing values (`Age`, `Cabin`, `Embarked`)
   - Convert categorical variables (`Sex`, `Embarked`) into numerical format
   - Feature scaling for numerical columns

2. **Exploratory Data Analysis (EDA)**
   - Distribution of survivors by gender, class, and age
   - Correlation heatmap between features

3. **Modeling**
   - Logistic Regression
   - Random Forest Classifier
   - Decision Tree Classifier
   - Evaluation Metrics: Accuracy, Confusion Matrix, Classification Report

4. **Results**
   - Achieved accuracy of ~X% with Random Forest
   - Identified important features: `Sex`, `Pclass`, `Age`, `Fare`

5. **Visualization**
   - Survival rate by class and gender
   - Age distribution by survival
   - Feature importance chart

---

## **Project 2: Stock Price Prediction**

### **Overview**
The Stock Price Prediction project predicts future stock prices using historical data. It demonstrates time-series forecasting using **LSTM (Long Short-Term Memory) networks** and data visualization techniques.

### **Dataset**
- Source: Historical stock data (Open, High, Low, Close, Volume)
- Format: CSV (inside `archive.zip`)
- Features:
  - `Date`, `Open`, `High`, `Low`, `Close`, `Volume`
- Target: `Close` price

### **Steps Performed**
1. **Data Preprocessing**
   - Convert `Date` to datetime
   - Sort by date
   - Handle missing values
   - Feature scaling (MinMaxScaler)

2. **Feature Engineering**
   - Optional: Moving Averages (MA10, MA50)
   - Optional: RSI, Bollinger Bands, Volume features

3. **Modeling**
   - LSTM model with two layers and dropout regularization
   - Sequence length = 60 days
   - Train-test split: 80%-20%
   - Loss function: Mean Squared Error

4. **Evaluation**
   - Root Mean Squared Error (RMSE)
   - Actual vs Predicted prices plot
   - Error analysis

5. **Visualization**
   - Candlestick chart
   - Moving averages with close price
   - Prediction vs actual line plot
   - Volume vs price chart
   - Rolling volatility plot
   - Correlation heatmap

6. **Future Prediction**
   - Predict next day stock price
   - Rolling predictions for multiple days

---

## **Requirements**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow mplfinance
