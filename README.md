# IDS705_ML_Final_Project_Cardiovasular_Disease



## Introduction
In recent decades, more young adults under 50 in the U.S. have been developing early risk factors for cardiovascular disease (CVD) and diabetes. CVD remains the leading cause of death and costs the healthcare system over $250 billion, yet many of its causes—like smoking, poor diet, and inactivity—are preventable. What’s worrying is that we still lack detailed data on how CVD affects younger adults, making it harder to understand and address the issue in this age group.

Meanwhile, diabetes is also on the rise. In 2021, nearly 15% of U.S. adults had diabetes, and rates in children and teens—especially among minority groups—have been climbing since 2002. What’s more, diabetes and CVD are deeply connected: people with diabetes are up to four times more likely to develop heart disease. They share many of the same risk factors, making prevention even more critical.

This project is timely and vital. As public health research funding declines, from both national and private sources, the ability to study, treat, and prevent these diseases is shrinking. That could have long-term effects not just on innovation, but on healthcare access and outcomes for millions of Americans.

---

## Goal/Objective
Our goal is to explore the contributors to the increase in young-onset CVD and diabetes prevalence, both in demographic profiles and lifestyle preferences. We will apply machine learning techniques to classify risk groups and potentially predict heart disease outcomes. Finally, we aim to investigate how data processing and machine learning models in CVD research compare to those used in diabetes studies and evaluate cross-domain applications.

## Datasets Introduction
Sources #1 and #2: UC Irvine Machine Learning Datasets 
Janosi, A., Steinbrunn, W., Pfisterer, M., & Detrano, R. (1989). Heart Disease [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C52P4X.

Source #3: All of Us Research 
National Institutes of Health, The All of Us Research Program Investigators, "The All of Us Research Program," N Engl J Med 2019;381:668-676, DOI: 10.1056/NEJMsr1809937

Source #4: WPRDC Diabetes Dataset 
Kahn, M.  Diabetes [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5T59G.
The Western Pennsylvania Regional Data Center Allegheny County [Dataset]. (2016). Diabetes. https://data.wprdc.org/dataset/diabetes 


Source #5: Diabetes prevalence from National Center for Health Statistics 
Diabetes prevalence and glycemic control among adults aged 20 and over, by sex, age, and race https://www.cdc.gov/nchs/hus/data-finder.htm 


---

## Experiments

### **Experiment 1: Analyzing Clinical and Anthropometric Measurements for CVD Risk Prediction**
- **Dataset**: CAIR-CVD-2025 (Bangladesh)
- Predict binary CVD risk using logistic regression (AUC, ROC)
- Predict continuous Framingham risk scores using linear regression (R², MSE)
- Goal: Identify key biomedical predictors of CVD to support prevention

### **Experiment 2: Comparing CVD Risk Prediction Models - PREVENT Equations vs. Machine Learning Models**
- **Dataset**: All of Us Research Program
- Compare PREVENT equations (baseline) to XGBoost and Neural Network
- Assess model fairness across race, sex, and ADI (social deprivation)
- Metric: AUC-ROC; Fairness analysis across demographic subgroups

### **Experiment 3: Diabetes and CVD - Confounder and Relationships**
- **Datasets**: UCI ML Diabetes, WPRDC, CDC Health Indicators
- Use Bootstrap CI, risk ratios, and causal inference (DoWhy, CausalForest)
- Examine cross-domain transferability of diabetes models to CVD prediction
- Identify personalized effects of diabetes on CVD via ITE estimation

### **Experiment 4: Differentiating Early-Onset vs. Late-Onset CVD Using Supervised Classification Algorithms**
- **Dataset**: All of Us Research Program
- Supervised models: Logistic Regression, Random Forest, XGBoost
- Classify early-onset (<55) vs. late-onset (≥55) CVD
- Identify risk factors most predictive of early-onset CVD

---

## Conclusions

- **Model Fairness**: PREVENT performs best overall but struggles in subgroups like Asian Males; ML models (XGBoost, NN) are more consistent and fair across subgroups, especially for Asian populations.
- **Diabetes-CVD**: Diabetes raises CVD risk at all ages; highest relative risk occurs under 50. Average CVD risk reduction if diabetes is removed is ~9%, but exceeds 40% for younger adults with low BMI.
- **Public Health Implication**: Younger adults (20–44) show rising diabetes rates—especially undiagnosed—posing a growing risk for early-onset CVD.
- **Targeted Interventions**: Preventing or treating diabetes in high-risk youth can yield large CVD risk reductions.

---

## Roles

- **Mu**: Compared PREVENT vs. machine learning; contributed to fairness analysis.
- **Lilah**: Investigated CAIR-CVD-2025 dataset, risk factors; revised shared outputs.
- **Sam**: Explored diabetes as a CVD risk factor; led causal inference modeling.
- **Su**: Focused on early vs. late-onset CVD; led subgroup pattern analysis.

---


## Repository Structure

```
project-root/
├── code/         # notebooks for modeling and analysis
├── data/         # raw and cleaned datasets
├── images/       # visualizations and figures
├── .gitignore
├── README.md
```

