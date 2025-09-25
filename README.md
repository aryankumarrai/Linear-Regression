# Housing Price Prediction using Linear Regression

This project focuses on building a simple Linear Regression model to predict the price of houses based on various features. It serves as a practical introduction to the entire machine learning modeling workflow, from data preprocessing to model evaluation.

---

## 🛠️ Tools and Libraries Used
* **Python**
* **Pandas** for data loading and manipulation.
* **Scikit-learn** for model building, data splitting, and evaluation.
* **NumPy** for numerical operations.

---

## 📋 Project Workflow

1.  **Data Loading and Inspection:**
    * The `Housing.csv` dataset was loaded into a pandas DataFrame.
    * Initial exploration was performed to understand the data's structure and check for missing values.

2.  **Data Preprocessing:**
    * **Categorical Feature Handling:** Text-based categorical features were converted into a numerical format suitable for modeling.
        * Binary variables ('yes'/'no') were mapped to `1` and `0`.
        * The multi-category `furnishingstatus` column was converted using one-hot encoding.

3.  **Data Splitting:**
    * The dataset was divided into features (**X**) and the target variable (**y**, `price`).
    * The data was split into an **80% training set** and a **20% testing set** using scikit-learn's `train_test_split` to ensure the model is evaluated on unseen data.

4.  **Model Training:**
    * A **Linear Regression** model from scikit-learn was instantiated.
    * The model was trained on the training data (`X_train`, `y_train`).

5.  **Prediction and Evaluation:**
    * The trained model was used to make price predictions on the test set (`X_test`).
    * The model's performance was evaluated using the following metrics:
        * **Mean Absolute Error (MAE):** Measures the average absolute difference between predicted and actual prices.
        * **Mean Squared Error (MSE):** Measures the average of the squared errors, penalizing larger errors more.
        * **R-squared ($R^2$) Score:** Indicates the proportion of the variance in the house prices that is predictable from the features.

---

## ✅ Results

The final model was able to explain approximately **65%** of the variance in housing prices (R-squared ≈ 0.65), providing a solid baseline for predicting house values based on the available features.
