# APPLIANCE-ENERGY-PREDICTION-
To build a predictive model to forecast the energy consumption of appliances in a low-energy house based on environmental and weather conditions.
## 📂 Dataset Description
The dataset consists of **19,735 observations** collected every 10 minutes over a period of 4.5 months.
* **Target Variable:** `Appliances` (Energy usage in Wh)
* **Features:** 29 features including:
    * **Internal Sensors:** Temperature and Humidity measurements for 9 different rooms (Kitchen, Living Room, Laundry, etc.).
    * **Weather Data:** External Temperature, Pressure, Humidity, Windspeed, and Visibility.
    * **Other:** Time-based features and random variables for benchmarking.

## 🛠 Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
* **Techniques:** Exploratory Data Analysis (EDA), Feature Engineering, Regression Modeling

## 🚀 Key Workflow
1.  **Exploratory Data Analysis (EDA):**
    * Analyzed energy consumption patterns over time.
    * Visualized correlations between internal sensor data and external weather conditions using heatmaps.
    * Identified that energy usage is heavily skewed, requiring transformation.
2.  **Data Preprocessing:**
    * **Scaling:** Applied MinMax and Standard Scaling to handle varying units (e.g., Temperature vs. Pressure).
    * **Feature Selection:** Removed non-predictive columns (e.g., 'lights', 'date') and highly collinear features.
    * **Outlier Treatment:** Handled outliers to improve model stability.
3.  **Model Training:**
    * Implemented multiple regression algorithms: **Linear Regression, Ridge, Lasso, Random Forest, and Extra Trees Regressor**.
    * Used Cross-Validation to ensure model robustness.

## 📊 Model Performance
The models were evaluated based on **R-squared (R²)** and **Root Mean Squared Error (RMSE)**.

| Model | R² Score | RMSE |
| :--- | :---: | :---: |
| **Extra Trees Regressor** | **0.64** | **66.5** |
| Random Forest Regressor | 0.59 | 71.2 |
| Linear Regression | 0.16 | 93.8 |
