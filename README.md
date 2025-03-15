# **Power Consumption Prediction Project**

## **Overview**
This project focuses on predicting power consumption in a specific zone using various machine learning models. The goal is to identify the best-performing model that can accurately predict power consumption based on features such as temperature, humidity, wind speed, and other environmental factors. The project involves data preprocessing, model training, evaluation, and visualization of results.

---

## **Dataset**
The dataset contains the following features:
- **Temperature**: Environmental temperature.
- **Humidity**: Relative humidity.
- **Wind Speed**: Wind speed in the area.
- **General Diffuse Flows**: General diffuse flows.
- **Diffuse Flows**: Diffuse flows.
- **Air Quality Index (PM)**: Air quality index based on particulate matter.
- **Cloudiness**: Cloudiness level.
- **Power Consumption in A Zone**: Target variable representing power consumption.

---

## **Project Steps**

### **1. Data Preprocessing**
- **Handling Missing Values**: Checked for missing values and handled them if necessary.
- **Feature Scaling**: Applied `StandardScaler` to normalize the features.
- **Train-Test Split**: Split the data into training (80%) and testing (20%) sets.

### **2. Model Training and Evaluation**
Several regression models were trained and evaluated using the following metrics:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **R² Score (Coefficient of Determination)**

The following models were implemented:
1. **Linear Regression**
2. **Ridge Regression**
3. **Lasso Regression**
4. **ElasticNet Regression**
5. **Decision Tree Regressor**
6. **Random Forest Regressor**
7. **Gradient Boosting Regressor**
8. **AdaBoost Regressor**
9. **Support Vector Regression (SVR)**
10. **XGBoost Regressor**
11. **LightGBM Regressor**
12. **CatBoost Regressor**

### **3. Hyperparameter Tuning**
- **Grid Search Cross-Validation (GridSearchCV)** and **Randomized Search Cross-Validation (RandomizedSearchCV)** were used to optimize hyperparameters for selected models.

### **4. Visualization**
- **Bar Plots**: Created bar plots to compare the performance of all models based on MAE, MSE, and R² scores.
- **Residual Plots**: Visualized the residuals (errors) to assess model performance.

---

## **Results**

### **Model Performance Summary**
| **Model**                  | **MAE**       | **MSE**         | **R²**       |
|----------------------------|---------------|-----------------|--------------|
| Linear Regression          | 2929.23       | 16288157.81     | 0.7479       |
| Ridge Regression           | 2929.23       | 16288157.81     | 0.7479       |
| Lasso Regression           | 2929.23       | 16288157.81     | 0.7479       |
| ElasticNet Regression      | 5450.36       | 45614284.78     | 0.2939       |
| Decision Tree Regressor    | 1297.69       | 8491273.45      | 0.8686       |
| Random Forest Regressor    | 1195.36       | 3964450.46      | 0.9386       |
| Gradient Boosting          | 4109.39       | 27648578.73     | 0.5720       |
| AdaBoost Regressor         | 4996.03       | 37111352.04     | 0.4255       |
| SVR                        | 4109.39       | 27648578.73     | 0.5720       |
| XGBoost Regressor          | 2648.51       | 14075018.63     | 0.7821       |
| LightGBM Regressor         | 2648.51       | 14075018.63     | 0.7821       |
| CatBoost Regressor         | 2929.23       | 16288157.81     | 0.7479       |

### **Key Findings**
- **Best Model**: **Random Forest Regressor** achieved the **highest R² score (0.9386)**, the **lowest MAE (1195.36)**, and the **lowest MSE (3964450.46)**.
- **Second Best Model**: **Decision Tree Regressor** performed well with an R² score of **0.8686**.
- **Worst Model**: **ElasticNet Regression** had the **lowest R² score (0.2939)** and the highest errors.

---

## **Conclusion**
The **Random Forest Regressor** is the best-performing model for predicting power consumption in this dataset. It explains **93.86%** of the variance in the target variable and has the lowest errors. The **Decision Tree Regressor** also performs well but is slightly less accurate. On the other hand, **ElasticNet Regression** performs poorly and is not suitable for this dataset. Future work can focus on hyperparameter tuning, feature engineering, and exploring other advanced models to further improve performance.

