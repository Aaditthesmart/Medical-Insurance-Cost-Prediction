# 🏥 Medical Insurance Cost Prediction using Decision Trees

## 📌 Project Overview
This project focuses on predicting **medical insurance charges** using supervised machine learning.  
The objective is to analyze how factors such as age, BMI, smoking habits, region, and number of children affect insurance costs, and to build a regression model that can make predictions on unseen data.

This project emphasizes understanding the **end-to-end machine learning workflow**, not just training a model.

---

## 🧠 What I Did in This Project

### 1️⃣ Data Loading & Inspection
- Loaded the dataset using **Pandas**
- Inspected:
  - Dataset shape
  - Column names
  - Data types
  - Missing values
  - Summary statistics

This step ensured the dataset was clean and suitable for modeling.

---

### 2️⃣ Exploratory Data Analysis (EDA)
Performed visual EDA to gain insights before modeling:

- **Smoking vs Charges**  
  Used a bar plot to compare average medical charges between smokers and non-smokers.

- **BMI vs Charges**  
  Used a scatter plot to observe the relationship between BMI and insurance charges.

- **BMI Distribution**  
  Used a histogram with KDE to understand the distribution of BMI values.

These plots helped in understanding feature importance and data behavior.

---

### 3️⃣ Feature Selection
- Defined **insurance charges** as the target variable.
- Selected the following features:
  - `age`
  - `sex`
  - `bmi`
  - `region`
  - `smoker`
  - `children`

Only relevant features were used to avoid noise and data leakage.

---

### 4️⃣ Train–Validation Split
- Split the dataset into training and validation sets using `train_test_split`.
- This simulates real-world scenarios where models are evaluated on unseen data.

---

### 5️⃣ Handling Categorical Variables
- Converted categorical features into numerical format using **one-hot encoding** (`pd.get_dummies`).
- Aligned validation features with training features using `reindex` to ensure consistent feature sets.

This step prevents errors and incorrect predictions due to mismatched columns.

---

### 6️⃣ Model Training
- Trained a **Decision Tree Regressor** on the training data.
- The model learned patterns between input features and insurance charges.

---

### 7️⃣ Model Evaluation
- Generated predictions on the validation dataset.
- Evaluated performance using **Mean Absolute Error (MAE)**.

MAE was chosen because it represents the average absolute prediction error in the same unit as the target variable.

---

### 8️⃣ Overfitting Analysis
- Calculated MAE on both training and validation datasets.
- Observed:
  - Very low training error
  - Significantly higher validation error

This indicates **overfitting**, a known behavior of unconstrained decision trees, and highlights the importance of proper model evaluation.

---

## 🛠 Tools & Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- scikit-learn

---

## 🎯 Key Learnings
- Importance of data inspection and EDA before modeling
- Handling categorical variables correctly in ML
- Understanding train vs validation performance
- Detecting overfitting using error metrics
- Building a complete ML workflow from scratch

---

## 🚀 Future Improvements
- Use ensemble models such as **Random Forest**
- Apply **cross-validation**
- Tune hyperparameters to reduce overfitting
- Convert preprocessing and modeling into an sklearn Pipeline
- Improve model generalization

---

## ✅ Conclusion
This project demonstrates a complete **machine learning pipeline**, from raw data analysis to model evaluation, with a strong focus on understanding model behavior rather than just achieving low error.

It serves as a solid foundation for more advanced machine learning techniques.
