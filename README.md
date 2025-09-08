# student-performance-classification
Predict student performance in secondary education (high school).
This data approach to student achievement in secondary education in two Portuguese schools. The data attributes include student grades, demographics, social characteristics, and school-related features. and it was collected by using school reports and questionnaires. Two datasets are provided regarding the performance in two distinct subjects: Mathematics (mat) and Portuguese language (por). 

In [Cortez and Silva, 2008], the two datasets were modeled under binary/five-level classification and regression tasks. Important note: the target attribute G3 has a strong correlation with attributes G2 and G1. This occurs because G3 is the final year grade (issued at the 3rd period), while G1 and G2 correspond to the 1st and 2nd period grades. It is more challenging to predict G3 without G2 and G1, but such a prediction is significantly more useful (see the paper source for more details).

student-performance-classification/
│── data/
  -student-mat.csv
  -student-por.csv
  - merge dataset
│── notebooks/
│   ├── student_performance_classification.ipynb
│── models/
│   ├── random_forest_model
│   ├── Logistic Regression
│   ├── Decision Tree
│── results/
|   ├── GridSearch
│   ├── confusion_matrix.png
│   ├── shap_summary.png
│── README.md
│── requirements.txt
