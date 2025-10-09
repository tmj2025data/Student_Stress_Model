# Student Stress Level Prediction - A Machine Learning Approach

##  Project Summary

This project develops a machine learning model to classify student stress levels into three categories: **Low, Medium, or High**.

The primary goal is to create an accurate and interpretable predictive tool that can serve as an **early warning system for educational institutions**. By identifying students at risk of high stress based on measurable behavioral, physical, and environmental factors, we can enable **timely and proactive mental health interventions**.

---

##  Key Results & Performance

The final model, a **Tuned Random Forest Classifier**, achieved **high performance**, exceeding the initial project target of 85% accuracy.

| Metric                | Result                 | Target Status  |
| --------------------- | ---------------------- | -------------- |
| **Final Accuracy**    | **90.9%**              | ✅ EXCEEDED     |
| **Model Improvement** | 1.82% gain from tuning | ✅              |
| **Target Classes**    | Low, Medium, High      | ✅              |
| **Top Predictor**     | Blood Pressure         | ✅ (Identified) |

---

##  Critical Stress Predictors (Feature Importance)

The Random Forest model provides valuable insights into which factors are most strongly associated with a student's stress level.

| Rank | Feature                          | Importance Score | Insight                                                                                                      |
| ---- | -------------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------ |
| 1    | **Blood Pressure**               | 0.157            | The strongest predictor, suggesting physiological markers often appear before conscious awareness of stress. |
| 2    | **Sleep Quality**                | 0.079            | A major bidirectional factor—poor sleep both causes and results from high stress.                            |
| 3    | **Academic Performance**         | 0.074            | Directly reflects the strain of the core educational mission.                                                |
| 4    | **Social Support**               | 0.067            | Lack of a support network significantly increases vulnerability to stress.                                   |
| 5    | **Teacher-Student Relationship** | 0.066            | A strong protective factor; positive interactions with faculty reduce stress load.                           |

---

##  Project Details

###  Dataset

* **Source:** Student Stress Monitoring Dataset (Kaggle)

* **File Used:** `StressLevelDataset.csv`

* **Rationale for Selection:**
  Clean, pre-encoded numeric features for 1,100 students with a **balanced class distribution** of the target variable (`stress_level`). Ideal for multi-class classification.

* **Number of Features:**  20 features (e.g., anxiety_level, sleep_quality, bullying) and 1 target variable (stress_level) for a total of 21 columns.

* **Feature Domains:** Physical health, mental health, academic life, and social environment.

###  Model Pipeline

* **Data Preparation:**

  * No missing values.
  * **StandardScaler** used for linear models.
  * Tree-based models used unscaled data.

* **Model Comparison:**

  * Tested **Logistic Regression**, **Random Forest**, and **XGBoost**.
  * **Random Forest** showed the best initial performance.

* **Hyperparameter Tuning:**

  * Used **GridSearchCV** to optimize Random Forest.
  * Final accuracy: **90.9%**

* **Final Model:**

  * `stress_predictor_model.pkl` (Ready for deployment)

---

##  Technical Requirements

The project notebook is implemented entirely in **Python** using the following libraries:

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn` (`sklearn`)
* `xgboost` (`xgb`)
* `joblib`
* `scipy`
* `statsmodels`

---

##  Recommendations for Application

Based on the model’s findings, educational institutions should focus proactive intervention efforts on:

* **Physiological Screening:**
  Integrate basic health checks (e.g., blood pressure monitoring) into routine student wellness programs to identify hidden stress.

* **Sleep Hygiene:**
  Develop and promote targeted programs to improve student sleep quality and routine.

* **Basic Needs Support:**
  Address food, housing, and financial insecurity—key stress contributors.

* **Faculty Training:**
  Train faculty to foster more positive teacher-student relationships, leveraging this as a **protective measure** against stress.

---

##  About the Author

* **Author:** Tanvi Joshi
* **Date:** 15th October 2025 (Project Completion)
* **Notebook:** `Student Stress Model.ipynb`
