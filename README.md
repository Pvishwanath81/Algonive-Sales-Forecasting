# Algonive-Sales-Forecasting

---

## 📌 Project Overview
This project predicts future sales using historical data with machine learning techniques.

Sales forecasting is important for businesses because it helps in planning inventory, managing demand, and making better decisions. The goal of this project is to analyze past sales patterns and predict future sales accurately.

---

## 📊 Dataset
I used the Rossmann Store Sales dataset from Kaggle, which contains store-level daily sales data.

The dataset includes features such as:
- Store
- DayOfWeek
- Sales
- Promo (promotion activity)
- StateHoliday / SchoolHoliday
- Date (used to extract time features)

The target column is:
- Sales (continuous value to predict)

---

## 🔍 Data Preprocessing
Before building models, I prepared the data:

- Converted Date column into datetime format
- Sorted data based on time (important for time-series)
- Removed rows where store was closed
- Converted holiday data into numerical format
- Created new features from Date (Year, Month, Day, DayOfWeek)
- Created lag feature (Sales_lag_7) to use past sales
- Removed rows with missing lag values
- Split data into training and testing sets using time-based split

This step ensures the data is clean and suitable for modeling.

---

## 📈 Exploratory Data Analysis (EDA)

I analyzed the data to understand patterns:

- Monthly Sales → Higher sales in November and December
- Weekly Sales → Sales vary across different days
- Promotions → Promo significantly increases sales
- Seasonal Patterns → Clear trends based on time

These insights helped understand how sales behave over time.

---

## 🤖 Models Used

### 1. Linear Regression
- Simple baseline model
- Assumes linear relationship between features and sales
- Easy to understand but limited performance

### 2. Random Forest
- Ensemble model using multiple decision trees
- Captures non-linear patterns
- Provides better accuracy than Linear Regression

---

## ⚙️ Model Improvement

Initially, the model used only basic time-based features.

To improve performance:
- Added lag feature (`Sales_lag_7`)

This allows the model to learn from past sales, which is very important in time-series forecasting.

---

## 📊 Feature Importance

Important features influencing sales:

- Sales_lag_7 (past sales)
- Promo (promotion activity)
- Store (store-specific behavior)
- Month (seasonality)

These features help the model understand sales patterns better.

---

## 📉 Model Comparison

I compared models using multiple metrics:

- Linear Regression → Basic performance
- Random Forest → Better accuracy and lower error

Random Forest performed better across all evaluation metrics.

---

## 🏆 Best Model

The best model is:

👉 **Random Forest**

Reason:
- Lower error (MAE, RMSE, MAPE)
- Better handling of complex patterns
- More reliable predictions

---

## 💡 Business Recommendations

Based on insights:

- Use past sales data for better forecasting
- Plan inventory for high-demand months (Nov–Dec)
- Use promotions strategically to increase sales
- Analyze store-level performance for better decisions

---

## 🧠 Conclusion

This project demonstrates a regression-based approach to time-series forecasting using historical data.

The addition of lag features improved model performance by allowing the model to learn from past trends. Random Forest performed better than Linear Regression due to its ability to capture complex patterns.

Further improvements can be made by adding more features and using advanced models.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib

---

## 📂 Project Structure

- sales_forecasting.ipynb → Complete code
- train.csv → Dataset used
- README.md → Project explanation

---

## 🙌 Final Note

This project helped me understand:
- Time-series forecasting
- Feature engineering (especially lag features)
- Model building and evaluation
- Real-world business problem solving
