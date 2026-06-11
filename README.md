# Student Performance Prediction using Machine Learning

## 1. Project Title
**Student Performance Prediction — Regression Analysis using Linear Regression, Decision Tree, and Random Forest**

Repository: synent-task8-student-performance-prediction-lavkumarjha

---

## 2. Problem Statement
Educational institutions want to understand which factors influence student academic performance and whether performance in one subject can help predict performance in another.

This project builds a regression model to predict a student's **Math Score** based on their **Reading Score**, **Writing Score**, and demographic/social attributes (gender, race/ethnicity, parental education level, lunch type, and test preparation course completion).

The goal is to:
- Identify key factors influencing math performance
- Build and compare multiple regression models
- Select the best-performing model and interpret its results

---

## 3. Dataset Information

- **Name:** Students Performance in Exams
- **Source:** [Kaggle — Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
- **Records:** 1001 rows (includes 1 duplicate row and a few missing values for cleaning practice)
- **Target Variable:** `math score`

| Column | Description |
|---|---|
| gender | Student's gender |
| race/ethnicity | Group classification (group A–E) |
| parental level of education | Highest education level of parent |
| lunch | Lunch type (standard / free-reduced) — socio-economic proxy |
| test preparation course | Whether student completed a prep course |
| math score | Math exam score (0–100) — **Target** |
| reading score | Reading exam score (0–100) |
| writing score | Writing exam score (0–100) |

---

## 4. Technologies Used
- Python 3.12
- Jupyter Notebook
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## 5. Project Workflow
1. **Data Loading & Inspection** — Load CSV, inspect structure, types, and summary statistics
2. **Data Cleaning** — Handle missing values, remove duplicates, verify data consistency
3. **Exploratory Data Analysis (EDA)** — Distributions, correlations, group comparisons
4. **Data Visualization** — Histograms, heatmaps, boxplots, scatter plots with insights
5. **Feature Engineering** — Ordinal encoding (parental education) and one-hot encoding (nominal categorical features)
6. **Train-Test Split** — 80/20 split
7. **Model Training** — Linear Regression, Decision Tree Regressor, Random Forest Regressor
8. **Model Evaluation** — RMSE, MAE, R² Score
9. **Model Comparison** — Compare all models and select the best
10. **Feature Importance** — Interpret which features drive math performance
11. **Conclusions & Future Scope**

---

## 6. Installation Steps

```bash
# Clone the repository
git clone git clone https://github.com/Lavkumarjha/synent-task8-studentperformanceprediction-lavkumarjha.git
cd synent-task1-student-performance-prediction-lavkumar

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 7. Usage Instructions

1. Ensure the dataset `StudentsPerformance.csv` is present in the `data/` folder.
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `notebook/student_performance_analysis.ipynb`.
4. Run all cells sequentially (Cell → Run All) to reproduce the full analysis, visualizations, model training, and evaluation.

---

## 8. Results

| Model | RMSE | MAE | R² Score |
|---|---|---|---|
| Linear Regression | 8.842 | 6.873 | 0.6680 |
| Decision Tree Regressor | 9.476 | 7.059 | 0.6186 |
| Random Forest Regressor | 8.847 | 6.710 | 0.6676 |

**Best Model: Linear Regression**

Linear Regression achieves the lowest RMSE and highest R² score, narrowly outperforming Random Forest. This is because the relationship between reading/writing scores and math score is predominantly linear, which Linear Regression captures efficiently without the added variance of tree-based models on this dataset size.

---
## 9. What I Learned

This project helped me understand the complete machine learning workflow, from data cleaning to model evaluation.

One thing that surprised me was how strongly reading and writing scores were related. I also observed that students who completed test preparation courses tended to perform better on average.

While comparing models, I learned that different algorithms can produce noticeably different results even on the same dataset.

## 10. Key Insights

1. **Reading and writing scores are the strongest predictors** of math performance — academic ability is consistent across subjects.
2. **Test preparation course completion** is associated with a meaningful score boost — an actionable intervention for schools.
3. **Lunch type** (socio-economic proxy) shows a measurable performance gap, highlighting potential equity concerns.
4. **Parental education level** correlates positively with student scores, suggesting home environment plays a supporting role.
5. **Gender** shows only a mild association with math scores in this dataset.

---

## 11. Future Improvements

- Hyperparameter tuning using GridSearchCV / RandomizedSearchCV
- Try Gradient Boosting models (XGBoost, LightGBM)
- Use k-fold cross-validation for more robust evaluation
- Incorporate additional features (study hours, attendance, school resources)
- Build multi-output models predicting reading/writing scores too
- Deploy the best model as a Streamlit/Flask web app
- Conduct a fairness/bias audit across demographic groups

---

## 12. Author Information

**Author:** Lav Kumar jha
**Project Type:** Internship Task — Data Science / Machine Learning
**Repository:** `synent-task1-student-performance-prediction-lavkumar`
