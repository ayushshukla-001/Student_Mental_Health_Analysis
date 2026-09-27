# Student Mental Health Analysis 🎓🧠

An exploratory data analysis (EDA) and machine learning project investigating the relationship between university students' academic life (course, year of study, CGPA) and their mental health (depression, anxiety, panic attacks).

## Introduction

The importance of mental health among college students cannot be overstated. As students leave behind familiar environments and enter university life, they experience significant emotional, social, and academic challenges. This project explores how factors such as course of study, year of study, gender, marital status, and academic performance (CGPA) relate to depression, anxiety, and panic attacks among students, and builds a classification model on the cleaned dataset.

## Dataset

- **File:** `Student Mental health.csv`
- **Records:** ~101 survey responses
- **Columns:**
  - `Timestamp` – when the response was submitted
  - `Gender` – Male / Female
  - `Age` – student age
  - `Course` – field of study
  - `Year` – current year of study
  - `CGPA` – CGPA range
  - `Marital status` – Yes / No
  - `Depression`, `Anxiety`, `Panic attack` – Yes / No
  - `Treatment` – whether the student sought specialist treatment

## Project Workflow

1. **Data Cleaning**
   - Standardized column names
   - Handled missing values
   - Removed duplicates and normalized inconsistent text (e.g. `year 1` vs `Year 1`, redundant course names)
   - Trimmed whitespace in the CGPA ranges
2. **Exploratory Data Analysis**
   - Pairplots and outlier checks
   - Year-wise breakdown of students per course
   - Depression / anxiety / panic attack rates by course and gender
   - Age distribution and density plots
   - Violin plots of mental health outcomes across year of study and CGPA
   - Correlation heatmaps
3. **Data Preprocessing**
   - Label encoding of categorical features
   - Feature/target split and train-test split
4. **Model Selection**
   - Built pipelines for Logistic Regression, Decision Tree, Random Forest, and SVC
   - Compared models using 10-fold cross-validation accuracy
5. **Model Evaluation**
   - Selected Random Forest as the best-performing model
   - Evaluated using accuracy, precision, recall, F1-score
   - Visualized results with a confusion matrix

## Key Findings

- Students enrolled in IT report the highest levels of anxiety, depression, and panic attacks among the surveyed courses.
- Female students report higher rates of depression and panic attacks than male students.
- Year 1 students (ages 18–20) show the highest rates of depression, anxiety, and panic attacks.
- Year 4 students report little to no depression, anxiety, or panic attacks.
- Marital status shows a notable association with depression.

## Technologies & Languages

**Language**
- Python 3

**Environment**
- Jupyter Notebook

**Libraries**
- `pandas` – data manipulation
- `numpy` – numerical computing
- `matplotlib` – data visualization
- `seaborn` – statistical data visualization
- `scikit-learn` – machine learning (pipelines, model selection, classifiers, metrics)
  - `LogisticRegression`, `DecisionTreeClassifier`, `RandomForestClassifier`, `SVC`, `LinearSVC`
  - `train_test_split`, `GridSearchCV`, `cross_val_score`
  - `LabelEncoder`
  - `accuracy_score`, `precision_score`, `recall_score`, `f1_score`, `classification_report`, `confusion_matrix`, `roc_curve`, `roc_auc_score`

## Project Structure

```
.
├── Student Mental health.csv          # Raw survey dataset
├── student-mental-analysis-eda-ml.ipynb  # EDA + ML notebook
└── README.md
```

## Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## Results

The Random Forest classifier achieved the best cross-validation performance among the four models tested (Logistic Regression, Decision Tree, Random Forest, SVC) and was selected for final evaluation on the held-out test set, with performance reported via accuracy, precision, recall, F1-score, and a confusion matrix.

## Acknowledgements

Dataset sourced from a student mental health survey (publicly available on Kaggle).
