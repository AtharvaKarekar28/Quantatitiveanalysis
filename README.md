# Analysis of the Impacts of Technology and Social Media on Mental and Physical Well-being

<div align="center">
  
![Syracuse University](images/graph_1.png)

**Author**: Atharva Bhushan Karekar  
**Institution**: Syracuse University  
**Course**: ITS 686 M001 Spring 2025  
**Instructor**: Professor Dilmore  
**Date**: May 8, 2025

</div>

---

## 📋 Table of Contents

- [Introduction](#introduction)
- [Research Questions](#research-questions)
- [Descriptive Overview](#descriptive-overview)
- [Inferential Analysis](#inferential-analysis)
  - [Q1: Gaming and Social Media vs Mental Health](#q1-gaming-and-social-media-usage-can-lead-to-poor-mental-health)
  - [Q2: Screen Time and Stress Level](#q2-is-screen-time-related-to-stress-level)
  - [Q3: Technology Usage and Sleep Duration](#q3-is-there-a-relationship-between-technology-usage-hours-and-sleep-duration)
  - [Q4: Social Media and Physical Activity](#q4-is-heavy-social-media-usage-associated-with-reduced-physical-activity)
  - [Q5: Support Systems and Wellbeing](#q5-access-to-support-systems-associated-with-better-physical-activity-or-sleep-patterns)
- [Key Findings & Recommendations](#key-findings--recommendations)
- [Conclusion](#conclusion)
- [Limitations](#limitations)
- [Appendix](#appendix)
- [Additional Resources](#additional-resources)

---

## 🌐 Introduction

In the modern era, technology is embedded in each and every individual's life. This report discusses the analysis between mental health and technological usage—examining how social media usage, screen time, gaming, and key indicators of mental and physical health, including stress levels, sleep patterns, and physical activity are related.

### Primary Objective

The primary objective of this analysis is to determine whether digital behavior patterns are significantly associated with mental health outcomes and lifestyle factors. The findings aim to provide data-driven insights into how modern technology engagement may influence well-being.

---

## ❓ Research Questions

This analysis addresses the following key questions:

1. **Can gaming and social media usage lead to poor mental health?**
2. **Is screen time related to stress level?**
3. **Is there a relationship between technology usage hours and sleep duration?**
4. **Is heavy social media usage associated with reduced physical activity?**
5. **Is access to support systems associated with better physical activity or sleep patterns?**

These questions guide our analysis on the impacts of technological usage on mental and physical health.

---

## 📊 Descriptive Overview

### Dataset Information

This report presents a comprehensive statistical analysis of the relationship between mental health and technology usage. The analysis consists of a dataset with **10,000 individuals**, including a wide range of variables related to:

- User demographics
- Technology engagement patterns
- Health indicators

### Key Variables Analyzed

**Numeric Variables:**
- `Social_Media_Usage_Hours`
- `Gaming_Hours`
- `Screen_Time_Hours`
- `Sleep_Hours`
- `Physical_Activity_Hours`
- `Support_System_Access`

### Statistical Summary

Variables were summarized using:
- **Measures of central tendency**: Mean, Median
- **Measures of dispersion**: Standard deviation, Range

**Findings:**
- Most variables displayed symmetric distributions with low impact on mental health
- `Gaming_Hours` and `Screen_Time_Hours` exhibited moderate skewness with outliers on the higher end
- Outliers were carefully examined using boxplots to understand their influence on regression results

### Visualization Methods

To support the statistical analysis, various visualizations were employed:
- **Boxplots**: Highlighted group differences
- **Line diagrams**: Made trends easier to interpret
- **2D plots**: Enhanced readability and understanding

These graphical tools, paired with statistical summaries, provide a clear and interpretable foundation for the inferential methods that follow.

---

## 🔬 Inferential Analysis

### Q1: Gaming and Social Media Usage Can Lead to Poor Mental Health?

**Response Variable**: `Mental_Health_Status`  
**Predictor Variables**: `Social_Media_Usage_Hours`, `Gaming_Hours`

#### Visual Analysis

**Gaming Hours:**

![Gaming Hours by Mental Health Status](images/graph_7.png)

- Gaming hours across all mental health statuses (Excellent, Fair, Good, Poor) are consistent at approximately 2.5-3 hours
- No substantial shifts or patterns suggesting increased/decreased gaming is associated with worsening mental health
- Visual observation suggests **no significant difference** in gaming behavior by mental health status

**Social Media Usage:**

![Social Media Usage by Mental Health Status](images/graph_6.png)

- Social media usage appears highly consistent across all mental health groups
- Median values around 4 hours per day with comparable interquartile ranges
- No notable shifts in usage levels across mental health categories
- Suggests **no clear association** between social media usage and mental health status

#### Statistical Tests

**One-Way ANOVA (Frequentist):**
- **P-values > 0.05** for both Social Media Hours and Gaming Hours
- **Conclusion**: No statistically significant difference in either variable on mental health status

**Bayesian ANOVA:**
- Social Media Usage: **BF = 0.00034**
- Gaming Hours: **BF = 0.00022**
- **Interpretation**: Extremely small Bayes Factors provide overwhelming evidence for the null hypothesis
- Data strongly support that neither gaming nor social media usage meaningfully varies with mental health status

**Multinomial Logistic Regression:**
- Neither gaming hours nor social media usage significantly predict mental health status
- All **p-values > 0.24**
- Effect sizes (coefficients) were very small
- **Conclusion**: Variations in time spent gaming or on social media are not meaningfully associated with mental health categories

---

### Q2: Is Screen Time Related to Stress Level?

**Response Variable**: `Stress_Level`  
**Predictor Variable**: `Screen_Time_Hours`

#### Visual Analysis

![Screen Time by Stress Level](images/graph_4.png)

- Median screen time is mostly consistent across all stress levels (Low, Medium, High)
- Higher stress level shows slightly wider range, indicating more variability
- Some high-stress users may be outliers with extreme screen time
- Overall suggests screen time may not dramatically differ with stress level

#### Statistical Tests

**Frequentist ANOVA:**
- **P-value >> 0.05**
- **Conclusion**: No statistically significant difference in screen time across stress levels
- Fail to reject null hypothesis

**Bayesian ANOVA:**
- **Bayes Factor (BF₁₀) = 0.0059**
- Data are approximately **170 times more likely** under null model
- **Strong evidence**: No meaningful relationship exists between screen time and stress level

**Ordinal Logistic Regression:**
- Coefficient: **β = 0.00059, p = 0.33**
- **Conclusion**: Screen time is not a statistically meaningful predictor of stress level

---

### Q3: Is There a Relationship Between Technology Usage Hours and Sleep Duration?

**Response Variable**: `Sleep_Hours`  
**Predictor Variable**: `Technology_Usage_Hours`

#### Visual Analysis

![Average Sleep Hours by Technology Usage](images/graph_3.png)

- Slight peak in sleep duration among users with 3-4 hours of technology usage
- Overall pattern is relatively flat
- Most groups average between **6.46 to 6.56 hours** of sleep
- No substantial shifts suggesting increased technology usage leads to more or less sleep
- **Visual conclusion**: No clear or significant relationship

#### Statistical Tests

**Frequentist ANOVA:**
- **P-value >> 0.05**
- **Conclusion**: No statistically significant difference in sleep duration across technology usage categories
- Technology usage is not significantly associated with sleep duration

**Bayesian ANOVA:**
- **Bayes Factor (BF₁₀) ≈ 2.9e-08**
- **Overwhelming support** for null model
- Extremely strong evidence against differences in sleep duration across technology usage levels

**Linear Regression:**
- Slope coefficient: **β = -0.0045** (not significant)
- For each additional hour of technology use, sleep decreases by only 0.0045 hours
- **R² = 0.000096** (virtually no predictive power)
- **Conclusion**: Effect size is negligible, not statistically significant

---

### Q4: Is Heavy Social Media Usage Associated with Reduced Physical Activity?

**Response Variable**: `Physical_Activity_Hours`  
**Predictor Variable**: `Social_Media_Usage_Hours`

#### Visual Analysis

![Average Physical Activity by Social Media Usage](images/graph_2.png)

- Average physical activity ranges from approximately **4.85 to 5.2 hours** per day across all social media usage groups
- Small fluctuations present but overall pattern is flat
- No consistent upward or downward trend
- Differences between bins appear random rather than systematic
- **Visual conclusion**: Increased social media usage is not clearly associated with reduced physical activity

#### Statistical Tests

**Bayesian Correlation Analysis:**
- **Bayes Factor (BF₁₀) = 0.024**
- Data are approximately **42 times more likely** under assumption of no correlation
- **Strong evidence** for null hypothesis

**Linear Regression:**
- Coefficient: **β = 0.0029, t(9998) = 0.23, p = 0.816**
- **R² ≈ 0.0000054** (virtually zero)
- Social media use explains almost none of the variation in physical activity
- **Conclusion**: Data do not support that heavier social media usage predicts lower physical activity levels

---

### Q5: Access to Support Systems Associated with Better Physical Activity or Sleep Patterns?

**Response Variables**: `Physical_Activity_Hours`, `Sleep_Hours`  
**Predictor Variable**: `Support_Systems_Access`

#### Visual Analysis

**Sleep Hours:**

![Sleep Hours by Support System Access](images/graph_5.png)

- Median sleep duration nearly identical for both groups (~6.5 hours/day)
- Interquartile ranges largely overlap
- **Conclusion**: Support system access is not associated with noticeable difference in sleep patterns

**Physical Activity:**

![Physical Activity by Support System Access](images/graph_8.png)

- Individuals with access to support systems display slightly higher median activity level
- Difference is modest but visible
- **Potential small positive association** between support access and physical activity

#### Statistical Tests

**T-Test Results:**

**Physical Activity:**
- **P-value = 0.027 < 0.05** ✅ Statistically significant
- Individuals with support systems engage in slightly more physical activity
- **Conclusion**: Significant positive association exists

**Sleep Hours:**
- **P-value > 0.05**
- No statistically significant difference between groups
- 95% confidence interval included zero
- **Conclusion**: Support system access does not significantly influence sleep duration

**Linear Regression Models:**

**Physical Activity:**
- Coefficient: **β = 0.13, t(9998) = 2.21, p = 0.027** ✅
- Individuals with support systems engage in **0.13 more hours** of physical activity per day
- **Statistically significant predictor**

**Sleep Hours:**
- Coefficient: **β = 0.028, t(9998) = 0.97, p = 0.333**
- **R² ≈ 0.00009** (virtually no variance explained)
- **Conclusion**: No significant effect of support system access on sleep

---

## 💡 Key Findings & Recommendations

### Major Findings

1. ✅ **Support systems positively impact physical activity** - Statistically significant relationship found
2. ❌ **No relationship** between gaming/social media and mental health
3. ❌ **No relationship** between screen time and stress levels
4. ❌ **No relationship** between technology usage and sleep duration
5. ❌ **No relationship** between social media usage and physical activity

### Recommendations for Community Leaders

Based on the analysis, we recommend:

1. **Invest in Local Support Systems**
   - Develop peer groups, wellness programs, or community centers
   - These showed measurable positive impact on physical activity
   - Focus resources here for maximum community health benefit

2. **Avoid Over-Focusing on Technology Reduction**
   - Data did not show strong link between technology usage and well-being
   - Unless other mental health concerns are evident
   - Balanced approach is recommended

3. **Promote Community Involvement**
   - Emphasize community involvement alongside physical activity
   - Balance technology use with social connections
   - Support overall health in rural and urban populations

---

## 🎯 Conclusion

Based on the findings from this analysis, **access to support systems plays a more consistent role in influencing physical activity than technology usage alone**. While common assumptions often link screen time and social media with poor mental or physical health, our results showed **no strong or reliable evidence supporting that narrative**. 

Instead, the presence of social support was associated with a **statistically significant increase in physical activity**, highlighting the value of human connection in promoting healthier lifestyles.

### Key Takeaway

> **Human connection and support systems matter more for physical health than limiting technology use.**

---

## ⚠️ Limitations

### Data Context Limitations

While the dataset was large (n=10,000), well-structured, and free from major missing values, it lacked key contextual variables:

- **Missing Variables:**
  - Socioeconomic status
  - Geographic location (urban vs. rural)
  - Chronic health conditions
  - Specific types or purposes of technology use
  - Quality of technology engagement

These variables could have provided deeper insights and more nuanced analysis.

### Methodological Limitations

1. **Observational Data**: Data is observational and self-reported
2. **Response Bias**: Potential for misreporting, especially regarding:
   - Health status estimates
   - Screen time accuracy
   - Mental health self-assessment
3. **Causality**: Cannot establish causal relationships, only associations
4. **Temporal**: Cross-sectional design limits understanding of changes over time

---

## 📈 LLM Usage Declaration

### Transparency in Analysis

**Research Question 1** (Gaming and Social Media vs. Mental Health):
- Used ChatGPT to help articulate visual interpretation of boxplots
- No results or data were generated by the model
- All statistical analyses performed independently

**Research Question 2** (Support Systems and Physical/Sleep Health):
- Used ChatGPT to assist in explaining model selection rationale
- Model output and interpretation based entirely on R analysis
- All statistical computations verified independently

**Research Question 3** (Screen Time and Stress Level):
- Used ChatGPT minimally to clarify ANOVA explanation
- Ensured terminology and results were described professionally
- All statistical results obtained and verified in R

---

## 📑 Appendix

### Key Plots

**Figure A1: Boxplot – Physical Activity by Support System Access**
- Shows individuals with support access engage in slightly more physical activity
- Visually supports t-test and regression findings indicating meaningful difference

**Figure A2: Line Plot – Average Sleep by Technology Usage**
- Demonstrates no substantial change in sleep across increasing tech usage
- Supports regression result showing no significant relationship

**Figure A3: Boxplot – Social Media Usage by Mental Health Status**
- Shows similar medians and spread across all mental health groups
- Visually reinforces conclusion that social media usage does not significantly impact mental health

### Highlighted Statistical Results

#### Physical Activity & Support Access
- **T-test**: p = 0.027 ✅
- **Regression**: β = 0.13, p = 0.027 ✅
- **Interpretation**: Individuals with support access are significantly more active

#### Sleep & Support Access
- **T-test**: p = 0.333
- **Regression**: β = 0.028, p = 0.333
- **Interpretation**: No meaningful difference in sleep duration

#### Mental Health & Tech Usage
- **ANOVA**: p > 0.48 for both variables
- **Bayes Factor**: BF ≈ 0.0002–0.0003 (strong support for no effect)
- **Multinomial Regression**: All p-values > 0.24
- **Conclusion**: No statistical relationship

#### Stress Level & Screen Time
- **ANOVA**: p = 0.20
- **Bayes Factor**: BF = 0.0059
- **Ordinal Regression**: β ≈ 0, p = 0.33
- **Conclusion**: No significant relationship

### Data Cleaning Notes

The dataset required minimal cleaning with key transformations:

**Variable Recoding:**
- `Support_Systems_Access`: Converted from categorical ("Yes"/"No") to binary numeric (1/0)
- `Mental_Health_Status`: Transformed to ordinal numeric scale (Excellent=1, Good=2, Fair=3, Poor=4)

**Missing Data Handling:**
- No missing values found in key variables
- No imputation or row removal necessary

**Outlier Inspection:**
- Visual inspections performed using boxplots
- High values noted but retained as they fell within realistic ranges
- Preserved natural variability of sample

**Variable Type Conversions:**
- All relevant variables confirmed as numeric
- Properly formatted for ANOVA, regression, and Bayesian analysis

---

## 📚 Additional Resources

**Dataset Source:**
- Kaggle – Mental Health and Technology Usage Dataset
- [https://www.kaggle.com/datasets/waqi786/mental-health-and-technology-usage-dataset](https://www.kaggle.com/datasets/waqi786/mental-health-and-technology-usage-dataset)

---

## 🛠️ Technologies Used

- **Statistical Analysis**: R Programming
- **Statistical Tests**: 
  - ANOVA (Frequentist and Bayesian)
  - Linear Regression
  - Ordinal Logistic Regression
  - Multinomial Logistic Regression
  - T-tests
- **Visualization**: R Graphics (ggplot2, base R plots)
- **Data Processing**: R tidyverse

---

## 📄 License

This project was developed for academic purposes as part of coursework at Syracuse University.

---

**Author**: Atharva Bhushan Karekar  
**Institution**: Syracuse University, School of Information Studies  
**Course**: ITS 686 M001 Spring 2025  
**Date**: May 2025
