# Insurance Project 2
abuja-insurance-analysis/

├── data/       
│   └── abuja_insurance.csv        
├── notebooks/   
│   └── insurance_eda.ipynb   
├── assets/    
│   └── plot_bmi.png            
├── ANALYSIS.md                  
└── README.md

# Insurance Claim Analysis Project

## Overview
This repository contains the Exploratory Data Analysis (EDA) of the 'MediClaim' insurance policy dataset for Abuja Insurance Company. The project focuses on identifying patterns in medical claims, BMI, smoking habits, and their correlation with insurance charges.

## Objectives
- Prove/Disprove if medical claims are higher for smokers.
- Compare BMI differences between genders.
- Analyze the relationship between smoking habits and geographic regions.
- Evaluate the impact of the number of children on BMI.

## Folder Structure
- `/data`: Contains the `abuja_insurance.csv` dataset.
- `/notebooks`: Contains the Jupyter Notebook where the cleaning and visualization were performed.
- `/assets`: Contains exported charts and images used in reports.

## Prerequisites
Ensure you have the necessary libraries installed:
```bash
pip install pandas numpy matplotlib seaborn







# Analysis Observations: MediClaim Dataset

This document summarizes the insights extracted from the `insurance_eda.ipynb` notebook regarding Abuja Insurance client data.

## 1. Primary Drivers of Insurance Costs
* **Smoking Status:** The analysis confirms that smoking is the most significant predictor of high insurance charges. On average, smokers pay significantly higher premiums than non-smokers, regardless of other variables.
* **BMI Impact:** There is a clear positive correlation between BMI and insurance charges. Specifically, clients with a BMI > 30 (obese category) see a sharper increase in costs, especially when combined with a smoking habit.

## 2. Demographic Breakdown
* **Gender Distribution:** The distribution of BMI across genders is relatively uniform. There is no significant statistical evidence to suggest that one gender has a higher average BMI or insurance cost than the other in this dataset.
* **Family Size:** Analysis of the 'children' feature shows that most of the dataset consists of individuals with 0 to 2 children. There is no strong linear correlation between the number of children and the total insurance charges.

## 3. Geographic & Behavioral Insights
* **Regional Variation:** While the number of claims is spread across regions, the 'Southeast' region shows a slightly higher concentration of smokers, which correlates with higher regional averages for insurance charges.
* **Interaction Effects:** The most expensive policyholders are those who fall into the high-BMI range *and* are active smokers. This group represents the highest risk segment for Abuja Insurance.

## 4. Key Statistical Findings
* **Correlation Coefficient:** The correlation between BMI and Charges is approximately **0.19** for the general population, but it jumps to over **0.75** when looking specifically at the smoker cohort.
* **Outliers:** The dataset contains several outliers representing extremely high medical costs; these are predominantly smokers with higher-than-average BMI.

## 5. Summary & Business Recommendations
* **Segmented Pricing:** Abuja Insurance could consider creating specialized wellness programs or "Stop Smoking" incentives that offer premium discounts, as this would directly address the primary cost drivers.
* **Risk Modeling:** Future predictive modeling should prioritize `smoker` and `bmi` as the primary features, as they explain the vast majority of the variance in `charges`.

