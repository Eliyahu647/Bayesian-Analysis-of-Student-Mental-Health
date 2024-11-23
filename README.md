# Bayesian Analysis Project: Student Stress, Anxiety, and Depression
---
### Project Description 📄

This project investigates the relationships between demographic and academic characteristics and mental health indicators (stress, anxiety, and depression) among university students. Using Bayesian analysis, the study identifies key predictors and patterns of these mental health conditions.

# Data Source 

The dataset includes survey responses from students in Bangladeshi universities, encompassing demographic and academic attributes, along with mental health metrics like stress, anxiety, and depression.

# Key Questions 

Is there a significant relationship between gender and depression levels?

How do demographic and academic variables (age, engineering background, academic year) influence stress and anxiety?

Does including stress and anxiety as predictors enhance the accuracy of depression prediction?

# Files in the Repository 📁

Project Data.csv: Contains the raw data used for the analysis.
### Stan Model Files:

model_q1.stan: Bayesian model for analyzing gender and depression.

model_q2.stan: Model for stress and anxiety with demographic and academic factors.

model_q3_1.stan & model_q3_2.stan: Models comparing depression prediction with and without stress/anxiety factors.

posterior_model.stan: Posterior analysis across all models.

### R Script:
sofi3.R: R script used for data preprocessing, running Stan models, and visualizations.

# Dashboards Overview 📊

Key Visualizations and Interpretations:

1. Gender and Depression:
Posterior Distribution of the Gender Coefficient:

Interpretation: Highlights the positive and significant relationship between gender and depression levels. Women report higher depression rates than men, with a posterior mean around 1.75.
Posterior Predictive Check:

The model aligns closely with the actual data, affirming its predictive capability for depression levels.

2. Stress and Anxiety Predictors:
Posterior Predictive Distribution for Stress:

Demonstrates the model's accuracy in capturing the distribution of stress across students.
Posterior Predictive Distribution for Anxiety:

Indicates that the model reasonably predicts anxiety levels.

3. Depression Prediction with Enhanced Models:
Model 1 vs. Model 2 Posterior Predictive Check:
Model 2 (with stress and anxiety factors) shows better alignment with observed depression levels compared to Model 1, supporting the inclusion of these factors.
Methodology 🛠️
Bayesian Modeling:
Likelihood Function:

Normal likelihood for all models, assuming continuous mental health metrics.
Prior Distributions:

Gender Effect (β_gender): 
𝑁
(
5
,
2
)
N(5,2)
Age Effect (β_age): 
𝑁
(
−
5
,
2
)
N(−5,2)
Stress/Anxiety Effects (β_stress, β_anxiety): 
𝑁
(
5
,
2
)
N(5,2)

Validation:

Effective sample size and R-hat values confirmed model convergence.
Sensitivity analysis indicated robust results despite prior changes.
# Key Findings 🔍
### Gender and Depression:

Women reported significantly higher depression levels than men.
This relationship remained robust across all prior sensitivity tests.

### Stress and Anxiety:

Age negatively correlated with stress and anxiety, indicating older students experience less of both.
Engineering students reported lower stress and anxiety than non-engineering peers.

### Depression Prediction:

Adding stress and anxiety metrics to demographic and academic predictors significantly improved model fit and accuracy.

# How to Use
### Data Analysis:
Open Project Data.csv to explore raw data.
### Model Execution:
Run sofi3.R to preprocess the data, fit Bayesian models, and generate visualizations.
### Customization:
Modify Stan models for further analysis or adapt prior assumptions based on new hypotheses.
