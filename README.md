# Student Performance Classification (with Explainability)

Predict final student performance (**G3**) in Portuguese secondary education using demographics, social factors, and school-related features. Two datasets are provided for distinct subjects: **Mathematics** (`student-mat.csv`) and **Portuguese** (`student-por.csv`).  
Data were collected from school reports and questionnaires. See: Cortez & Silva (2008).

> Important: `G3` is strongly correlated with `G1` and `G2` because they are 1st, 2nd, and final period grades.  
> For a realistic task, we **do not use G1 or G2** as inputs when predicting G3.

---
## Data

- `data/student-mat.csv` — Mathematics subject  
- `data/student-por.csv` — Portuguese subject  
- Delimiter: **semicolon** `;`

Each file contains demographics, social context, study habits, support programs, and final grades.## Project Structure

```plaintext
student-performance-classification/
├── data/
│   ├── student-mat.csv
│   └── student-por.csv
├── notebooks/
│   └── student_performance_classification.ipynb
├── models/
│   ├── random_forest_model.joblib
│   ├── logistic_regression_model.joblib
│   └── decision_tree_model.joblib
├── results/
│   ├── GridSearch/
│   ├── confusion_matrix.png
│   └── shap_summary.png
├── README.md
└── requirements.txt

## Goal

Binary classification: **Pass vs Fail** based on final grade `G3`.  
- Label: `Pass = 1 if G3 >= 10 else 0` (Portuguese 0–20 scale).  
- Inputs: all features **except** `G1`, `G2`, `G3`.

We also report feature importance with **SHAP** for transparency.
## Result
---
<img width="790" height="940" alt="image" src="https://github.com/user-attachments/assets/7a8e98f3-4077-49a3-a96a-0d86a253aded" />
## Explainability

We used **SHAP (SHapley Additive exPlanations)** to interpret model predictions.  

Key features influencing student success include prior failures, absences, extracurricular activities, and parental education levels.

)


