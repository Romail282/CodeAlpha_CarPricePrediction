Car Price Prediction 🚗

A machine learning project that predicts the selling price of used cars based on features like present price, age, mileage, fuel type, transmission, and ownership history.

This project was completed as **Task 3** of my Data Science Internship at **CodeAlpha**.

📌 Problem Statement

Given details about a used car, build a regression model that accurately predicts its resale selling price.

📊 Dataset

301 used car listings with the following features:

- Car_Name, Year, Present_Price, Driven_kms, Fuel_Type, Selling_type, Transmission, Owner
- **Target:** Selling_Price (in lakhs)

🛠️ Feature Engineering & Preprocessing

- Converted `Year` into `Car_Age` (a more directly meaningful feature than raw manufacturing year)
- Dropped `Car_Name` due to high cardinality (too many unique values relative to dataset size)
- One-hot encoded categorical features (`Fuel_Type`, `Selling_type`, `Transmission`) into numeric columns

🤖 Model

- **Algorithm:** Linear Regression
- **Train/Test Split:** 80% training, 20% testing
- **R² Score:** 0.849
- **Mean Absolute Error:** 1.216 lakhs

🔍 Key Insights

- **Fuel type had the strongest standalone effect on price** — diesel cars commanded a significant premium over petrol, more than raw mileage or present price contributed individually
- Manual transmission cars sold for less than automatics, and cars sold by individual sellers (vs. dealers) also fetched lower prices
- The model performs very well for typical, moderately priced cars, but is less accurate for high-end outliers — a known limitation of Linear Regression on skewed price distributions
- Linear Regression can technically predict negative prices for very low-value cars, since it has no built-in floor at zero — an important caveat when using this model in practice

🛠️ Tools & Libraries

- Python, Pandas, Matplotlib, Scikit-learn

🚀 How to Run

1. Clone this repository
2. Open `CodeAlpha_CarPricePrediction.ipynb` in Jupyter Notebook or Google Colab
3. Ensure `Car Data.csv` is in the same directory
4. Run all cells

📝 Key Learnings

- How to engineer more meaningful features from raw data (Year → Age)
- How to encode categorical variables for machine learning models
- The difference between R² and Mean Absolute Error, and how to interpret each
- How to read model coefficients to understand which features drive predictions
- Recognizing the practical limitations of a model, not just its headline accuracy score

🔗 Author

Romail — Computer Science student exploring Data Science  
Data Science Intern @ CodeAlpha

---
*This project is part of the CodeAlpha Data Science Internship.*
