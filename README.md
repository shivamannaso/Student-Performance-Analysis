# 📚 IDS Mini-Project: Student Performance Analysis

## Overview

This project is an **Intelligent Data Systems (IDS) mini-project** focused on analyzing student performance and predicting their final grade. The core goal is to use data science techniques to identify key factors that influence a student's final marks (G3) and provide an automated way to predict performance early.

The prediction model achieved high accuracy, allowing for the early identification of students who may be at risk.

## Dataset

* **Source File:** `student.csv`
* **Size:** Contains data for 395 students across 33 different academic and personal attributes.
* **Key Columns:**
    * **G1** (First period marks)
    * **G2** (Second period marks)
    * **G3** (Final marks - The target variable for prediction)
    * **studytime** (Weekly study hours)
    * **absences** (Number of days absent)

## Methodology and Analysis

The analysis was performed in the `StudentP (1).ipynb` Jupyter Notebook.

1.  **Feature Engineering:**
    * The `studytime` column was converted into real `study_hours`.
    * An **`attendance_rate`** feature was created from the `absences` column.

2.  **Exploratory Data Analysis (EDA):**
    * An EDA was conducted, including a correlation heatmap and scatter plots, which showed that **G2 (second period marks) has the strongest relation to G3**.

3.  **Modeling:**
    * **Linear Regression (Baseline):** A model was built using the features: `G3 ~ G2 + study_hours + attendance_rate`.
    * **Ridge Regression (Advanced):** A more robust model was implemented using OneHotEncoding for categorical variables and RidgeCV for regularization to reduce overfitting.

## Results

Both models demonstrated strong predictive power for the final grade (G3).

| Model Metric | Value |
| :--- | :--- |
| **R² Score** (Linear Regression) | $\approx 0.86$ |
| **Mean Absolute Error (MAE)** | $\approx 0.74$ |

### Key Findings
* **G2 is the strongest predictor** of a student’s final marks (G3).
* More study hours generally lead to better performance.
* Higher absence rates are correlated with lower final marks.

## Repository Contents

| File | Description |
| :--- | :--- |
| `StudentP (1).ipynb` | The executable analysis code (Jupyter Notebook) |
| `student.csv` | The raw student performance dataset |
| `IDS_PPT.pptx` | The final project presentation slides |
| `README.md` | This project summary |