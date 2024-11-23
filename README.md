---

# Bayesian Analysis of Student Mental Health 📊 

This project explores the relationship between demographic and academic factors and mental health variables (stress, anxiety, and depression) among university students. Using Bayesian statistical models, we uncover key insights about how these variables interact and impact students' well-being.

---

## Files in this Repository📁 
- **Project Data.csv**: Dataset containing demographic, academic, and mental health information (stress, anxiety, depression scores).
- **Stan Files**:
  - `model_q1.stan`: Examines the effect of gender on depression levels.
  - `model_q2.stan`: Investigates how age, engineering studies, and academic year influence stress and anxiety.
  - `model_q3_1.stan` and `model_q3_2.stan`: Compare predictors of depression with and without stress/anxiety metrics.
  - `posterior_model.stan`: Combines models for advanced posterior predictive checks.

---

## Research Questions🔍 

### **1. Gender and Depression**
**Question**: Is there a significant difference in depression levels between men and women?  
**Insights**:
The posterior analysis shows a significant effect of gender on depression levels, indicating that women experience higher levels of depression on average.  

#### Visualization
![Posterior Distribution of Gender Coefficient](https://raw.githubusercontent.com/username/repository-name/main/gender_coefficient.png)

---

### **2. Demographics and Stress/Anxiety**
**Question**: How do age, field of study (engineering vs. non-engineering), and academic year affect stress and anxiety levels?  
**Insights**:
- Younger students tend to report higher stress and anxiety levels.
- Engineering students experience lower stress and anxiety compared to students in other fields.
- Advanced academic years correlate with increased levels of stress and anxiety.

#### Posterior Predictive Check for Stress
![Posterior Predictive Check for Stress](https://raw.githubusercontent.com/username/repository-name/main/stress_posterior_check.png)

#### Posterior Predictive Distribution for Stress and Anxiety
![Posterior Predictive Distribution for Stress](https://raw.githubusercontent.com/username/repository-name/main/stress_distribution.png)  
![Posterior Predictive Distribution for Anxiety](https://raw.githubusercontent.com/username/repository-name/main/anxiety_distribution.png)

---

### **3. Improved Prediction of Depression**
**Question**: Does adding stress and anxiety metrics improve the prediction of depression compared to demographic and academic variables alone?  
**Insights**:
Including stress and anxiety as predictors significantly enhances the depression model's performance and provides a more accurate prediction of depression levels.

#### Posterior Predictive Check for Depression
![Posterior Predictive Check for Depression](https://raw.githubusercontent.com/username/repository-name/main/depression_posterior_check.png)

---

## Tools and Methods🛠️ 

1. **Bayesian Models**:
   - Built and estimated using Stan with MCMC sampling.
   - Models include hierarchical structures to account for variability across individuals.

2. **Model Evaluation**:
   - **Prior Predictive Checks**: Ensure reasonable assumptions before running models.
     ![Prior Predictive Check](https://raw.githubusercontent.com/username/repository-name/main/prior_predictive_check.png)
   - **Posterior Predictive Checks**: Validate the fit of models to observed data.
     ![Posterior Predictive Check](https://raw.githubusercontent.com/username/repository-name/main/posterior_predictive_check.png)

3. **Visualization**:
   - Visualized posterior distributions, predictive checks, and key results using Python and R.

---

## 📊 Key Insights
1. **Gender**:
   - Women have significantly higher depression levels than men.
2. **Stress and Anxiety**:
   - Younger students and those in advanced years are more prone to stress and anxiety.
   - Engineering students report lower levels of these variables compared to non-engineering students.
3. **Depression Prediction**:
   - Models that include stress and anxiety metrics perform better than those relying solely on demographics.

---

---

## 🔗 Repository Structure
- **Data**: Contains the cleaned dataset used in the analysis.
- **Models**: Stan files for each Bayesian model.
- **Results**: Visualizations of posterior distributions and predictive checks.

---
