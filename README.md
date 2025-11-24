# 🎓 Student Performance Prediction Using Ensemble Learning

This repository presents an end-to-end **data analytics and machine learning study** on predicting student academic outcomes using demographic and preparatory variables.  
It was developed in **R** as part of my Data Analytics coursework (DA5030) and refined as a showcase project for my data science portfolio.

---

## Motivation

Education is one of the strongest predictors of social mobility, yet students’ achievements are influenced by a complex mix of factors — family background, resources, and motivation.  
The motivation behind this project was to **quantify those influences** and determine which measurable features (such as parental education or test-prep participation) most strongly impact performance.

My personal goal was twofold:
1. **Demonstrate technical fluency** in R’s data-science ecosystem — from cleaning and visualizing data to building ensemble models.
2. **Communicate insights clearly**, bridging technical output with meaningful educational interpretation.

---

## Project Objectives

1. Explore how demographic factors affect student test outcomes.  
2. Build multiple machine learning models to predict performance.  
3. Compare the strengths of ensemble methods versus traditional baselines.  
4. Produce an interactive, shareable HTML report that tells a coherent data story.  

---

## Technical Stack

| Category | Tools / Libraries |
|-----------|------------------|
| **Programming** | R, RMarkdown |
| **Data Manipulation** | `tidyverse`, `dplyr`, `tidyr` |
| **Visualization** | `ggplot2`, `corrplot` |
| **Modeling** | `caret`, `randomForest`, `gbm`, `e1071` |
| **Reporting** | `knitr`, `rmarkdown` |

The project is fully reproducible on any system with R installed and includes all data, code, and outputs.

---

##  Methodology

### 1. Data Understanding
The dataset (`students_performance_data.csv`) includes key attributes:
- **Gender**
- **Parental level of education**
- **Lunch type (standard vs free/reduced)**
- **Test preparation course completion**
- **Math, Reading, and Writing scores**

Basic descriptive statistics and visual exploration (histograms, boxplots, correlations) were performed to detect patterns and outliers.

---

### 2. Data Preprocessing
- Converted categorical variables into factors.  
- Handled missing or inconsistent entries.  
- Scaled numeric scores for model comparability.  
- Created a composite “average score” variable representing overall academic performance.

---

### 3. Exploratory Data Analysis (EDA)
EDA revealed:
- Students who completed **test preparation courses** scored significantly higher.  
- **Parental education** correlated positively with student scores.  
- **Gender differences** were subtle but consistent across reading and writing metrics.  

Visuals (produced via `ggplot2`) helped communicate these patterns intuitively.

---

### 4. Modeling and Evaluation
Three main models were trained and tuned using **caret**:
- **Logistic Regression** – baseline for interpretability  
- **Random Forest** – robust tree-based ensemble model  
- **Gradient Boosting (GBM)** – sequential ensemble learning  

Performance metrics:
- Accuracy
- Precision / Recall
- Confusion Matrix
- Variable Importance ranking  

####  Results Summary
| Model | Accuracy | Key Notes |
|-------|-----------|-----------|
| Random Forest | **91%** | Highest accuracy, excellent generalization |
| Gradient Boosting | **89%** | Slightly lower but stable under cross-validation |
| Logistic Regression | **84%** | Provided strong interpretability baseline |

**Top predictors**: parental education level, test preparation status, and lunch type.

---

### 5. Visualization & Interpretation
- Feature importance plots emphasized the social and environmental context behind academic achievement.  
- Correlation heatmaps highlighted inter-subject score relationships.  
- Comparative bar charts illustrated model accuracies.

These elements are compiled in the rendered HTML report for non-technical audiences.

---

## Repository Structure

| File | Description |
|------|--------------|
| `student_performance_analysis.Rmd` | RMarkdown source file containing the full workflow, from import to model building. |
| `student_performance_report.html` | Rendered interactive report (open directly in a browser). |
| `students_performance_data.csv` | Dataset used for training and testing models. |
| `README.md` | This documentation file. |

---


