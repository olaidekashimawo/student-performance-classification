# Student Performance Classification (with Explainability)

Predict final student performance (**G3**) in Portuguese secondary education using demographics, social factors, and school-related features. Two datasets are provided for distinct subjects: **Mathematics** (`student-mat.csv`) and **Portuguese** (`student-por.csv`).  
Data were collected from school reports and questionnaires. See: Cortez & Silva (2008).

> Important: `G3` is strongly correlated with `G1` and `G2` because they are 1st, 2nd, and final period grades.  
> For a realistic task, we **do not use G1 or G2** as inputs when predicting G3.

---

## Project Structure
---
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

---

## Data

- `data/student-mat.csv` — Mathematics subject  
- `data/student-por.csv` — Portuguese subject  
- Delimiter: **semicolon** `;`

Each file contains demographics, social context, study habits, support programs, and final grades.

---

## Quickstart

### 1) Install

```bash
python -m venv .venv && source .venv/bin/activate   # on Windows: .venv\Scripts\activate
pip install -r requirements.txt
