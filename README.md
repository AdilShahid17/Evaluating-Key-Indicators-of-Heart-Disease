# Evaluating-Key-Indicators-of-Heart-Disease

## Table of Contents
1. [Project Proposal](#project-proposal)
2. [Introduction to the Dataset](#introduction-to-the-dataset)
3. [Data Exploration and Cleaning](#data-exploration-and-cleaning)
4. [Exploration and Questions](#exploration-and-questions)
5. [Machine Learning](#machine-learning)
6. [Conclusion](#conclusion)
7. [References](#references)

## Project Proposal

### Evaluating Key Indicators of Heart Disease
The goal of the project is to test different factors to detect the ones that have the greatest impact on heart disease, which will ultimately serve in helping us find ways to prevent them. We also want to identify which demographics (race and gender) are more at risk, as well as which lifestyle factors are most relevant to the prevalence of heart disease. All of these will help in providing relevant and timely support to the groups most at risk.

We are interested in this problem because heart disease is one of the leading causes of death, leading to ~930,000 deaths/year in the US alone, and $229 billion in healthcare costs/year according to CDC. Identifying the factors that play a role in causing heart diseases will help reduce these losses.

### Data Source
The dataset comes from the CDC and is a major part of the Behavioral Risk Factor Surveillance System. The original dataset of nearly 300 variables was reduced to just about 20 variables by Kamil Pytlak on Kaggle. We will try using the original file from the CDC for the purposes of our analysis, linked here (the file is in ASCII format, and we will discuss with our supervisor on how best to access it): [CDC BRFSS 2020 Data](https://www.cdc.gov/brfss/annual_data/2020/files/LLCP2020ASC.zip).

## Introduction to the Dataset

The dataset has 319,795 rows and 18 columns. Each row represents respondents to the survey. The target value is HeartDisease, indicating whether the respondent ever reported having heart disease. Each column is an indicator that might have a relationship with heart disease.

| Column           | Data Type | Description                                                                          |
|------------------|-----------|--------------------------------------------------------------------------------------|
| HeartDisease     | Categorical | Ever reported having coronary heart disease or myocardial infarction                 |
| BMI              | Numeric    | Body Mass Index (BMI)                                                                |
| Smoking          | Categorical | Smoked at least 100 cigarettes in entire life (5 packs = 100 cigarettes)             |
| AlcoholDrinking  | Categorical | Heavy drinkers (adult men having more than 14 drinks per week and adult women having more than 7 drinks per week) |
| Stroke           | Categorical | (Ever told) (had) a stroke                                                           |
| PhysicalHealth   | Numeric    | For how many days during the past 30 was your physical health not good                |
| MentalHealth     | Numeric    | For how many days during the past 30 was your mental health not good                  |
| DiffWalking      | Categorical | Whether having serious difficulty walking or climbing stairs                        |
| Sex              | Categorical | Male or female                                                                      |
| AgeCategory      | Categorical | Fourteen-level age category                                                         |
| Race             | Categorical | Race/ethnicity value                                                                |
| Diabetic         | Categorical | (Ever told) (you had) diabetes                                                      |
| PhysicalActivity | Categorical | Whether doing physical activity or exercise during the past 30 days other than regular job |
| GenHealth        | Categorical | How would you rate your health in general                                           |
| SleepTime        | Numeric    | Hours of sleep get in a 24-hour period on average                                     |
| Asthma           | Categorical | (Ever told) (you had) asthma                                                        |
| KidneyDisease    | Categorical | Were you ever told you had kidney disease, not including kidney stones, bladder infection, or incontinence |
| SkinCancer       | Categorical | (Ever told) (you had) skin cancer                                                   |

## Data Exploration and Cleaning

The initial steps involved data exploration and cleaning, focusing on:
- Checking for missing values
- Exploring numeric and categorical data
- Cleaning categorical data (e.g., merging similar categories)

## Exploration and Questions

### Key Findings
- **Race and Heart Disease**: Significant disparities in heart disease rates were found among different races.
- **Stroke and DiffWalking**: These were identified as main effects contributing to heart disease, especially among American Indian/Alaskan Native populations.
- **Gender Disparities**: Men showed higher rates of heart disease compared to women, particularly in the White race category.
- **Combined Effects**: Combined analysis of factors like sleep time, alcohol drinking, and general health provided deeper insights into the risk factors for heart disease.

### Visualizations
Several visualizations were created to explore these relationships, including bar plots, point plots, and scatter plots.

## Machine Learning

### Feature Engineering
Features were engineered from categorical variables and numeric transformations to prepare for machine learning models.

### Random Forest
A Random Forest classifier was used to identify feature importance, highlighting age, stroke, and difficulty walking as key predictors.

### Principal Component Analysis (PCA)
PCA was performed to reduce dimensionality, identifying key components that explain the variance in the data.

### K-Means Clustering
K-means clustering was applied to the PCA-transformed data to identify clusters within the data, aiding in the understanding of different risk groups.

## Conclusion

We explored the disparity in heart disease between races and genders, identifying key factors such as stroke, difficulty walking, and general health that contribute to heart disease. Our machine learning analysis using Random Forest and PCA helped in identifying important predictors and clustering similar groups. Further exploration is needed to fully understand the underlying causes and disparities in heart disease rates.

## References

- [CDC Heart Disease Facts](https://www.cdc.gov/heartdisease/facts.htm)
- [Kaggle: Personal Key Indicators of Heart Disease Dataset](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
- [CDC BRFSS 2020 Data](https://www.cdc.gov/brfss/annual_data/2020/files/LLCP2020ASC.zip)
- [CDC Quality Assurance](https://www.cdc.gov/os/quality/support/info-qual.htm)
- [CDC Sleep Recommendations](https://www.cdc.gov/sleep/about_sleep/how_much_sleep.html)
- [CDC Healthy Weight](https://www.cdc.gov/healthyweight/assessing/index.html#:~:text=If%20your%20BMI%20is%20less,falls%20within%20the%20obese%20range)
- [Study on Mental Stress and Heart Disease in Europe](https://pubmed.ncbi.nlm.nih.gov/12721140/)

---

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yourusername/your-repo-name/blob/main/your-notebook.ipynb)
