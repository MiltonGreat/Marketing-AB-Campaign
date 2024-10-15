# Marketing A/B Testing Analysis

This project conducts an A/B test to analyze the impact of changes in marketing strategies and determine the effectiveness of different marketing approaches in improving customer conversion rates.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [Project Workflow](#project-workflow)
  - [Data Preprocessing](#data-preprocessing)
  - [Feature Engineering](#feature-engineering)
  - [Descriptive and Visual Analysis](#descriptive-and-visual-analysis)
  - [A/B Test Analysis](#ab-test-analysis)
  - [Statistical Testing](#statistical-testing)
  - [Power and Effect Size](#power-and-effect-size)
  - [Business Recommendations](#business-recommendations)
- [Usage](#usage)
- [License](#license)

## Overview

This project analyzes a marketing campaign's performance through A/B testing, comparing two different groups exposed to different ad strategies to measure their impact on customer conversion rates. The project evaluates the conversion rates between the control (ad) and treatment (psa) groups, uses statistical tests to determine significance, and calculates effect sizes and power for robust business recommendations.

## Dataset

The dataset contains information related to the marketing campaign, including:
- **Test group**: Whether a user was exposed to a specific ad or a public service announcement (PSA).
- **Conversion status**: Whether the user converted (1) or did not convert (0).
- **Total ads**: The number of ads the user was exposed to.
- **Most ads day/hour**: The time when users saw most ads, including the day of the week and the hour.

## Objectives

- **Conduct an A/B test** to determine if there is a significant difference in conversion rates between the control (ad) and treatment (psa) groups.
- **Statistically analyze** the effectiveness of marketing strategies and draw meaningful business conclusions.
- **Calculate the effect size** to understand the practical significance of the observed difference between groups.
- **Perform power analysis** to ensure that the sample size is sufficient for reliable results.

## Key Features

1. **Data Cleaning**: Remove duplicates, handle missing values, and ensure consistent formatting of columns.
2. **Feature Engineering**: Generate new features such as `time_of_day` (segmentation by hour) and `ads_intensity` (categorization of ad exposure into low, medium, high).
3. **Visualization**: Provide clear visualizations of conversion rates, total ads viewed, and conversion rates across different time segments.
4. **A/B Testing**: Perform chi-square tests to determine if the differences between control and treatment groups are statistically significant.
5. **Power Analysis**: Use power analysis to verify the reliability of the test results.

## Project Workflow

### Data Preprocessing
- **Loading and inspecting the dataset**: Data is extracted from a ZIP file, and basic checks for missing values, duplicates, and data types are performed.
- **Cleaning**: Remove unnecessary columns, ensure consistent formatting, and convert categorical variables where needed.

### Feature Engineering
- **Time segmentation**: Create a feature `time_of_day` to categorize ad exposure into segments like Morning, Afternoon, Evening, and Night.
- **Weekend flag**: Generate a binary column to indicate if the ad exposure occurred on a weekend.
- **Ads intensity**: Categorize total ads exposure into `Low`, `Medium`, and `High`.

### Descriptive and Visual Analysis
- **Conversion rates by group**: Visualize and compare conversion rates between the test groups (control and treatment).
- **Ad exposure analysis**: Compare the number of ads seen between groups using box plots.
- **Time of day analysis**: Analyze conversion rates by different time segments.

### A/B Test Analysis
- **Group comparison**: Compare the sizes and conversion rates of the test and control groups.
- **Chi-square test**: Perform a chi-square test to determine if there is a statistically significant difference in conversion rates between the two groups.

### Statistical Testing
- **Contingency table**: Generate a table summarizing the conversion counts in the control and treatment groups.
- **Chi-square test**: Calculate the chi-square statistic, degrees of freedom, and p-value to assess statistical significance.

### Power and Effect Size
- **Power analysis**: Ensure the test has sufficient statistical power to detect differences using power analysis.
- **Effect size (Cohen's h)**: Calculate Cohen's h to assess the magnitude of the difference in conversion rates between the groups.

### Business Recommendations
- Based on statistical significance, effect size, and conversion rates, make actionable business recommendations for adopting or revising marketing strategies.

### Part 2: Code Explanation and Insights

#### Code Overview:
The code is performing an **A/B testing analysis** on a marketing campaign dataset to evaluate how changes in marketing strategies affect **conversion rates**. The two groups compared are:
- **Control group** ("ad") exposed to the original marketing strategy.
- **Treatment group** ("psa") exposed to a new strategy.

##### Key Steps:
1. **Data Cleaning**: 
   - Unnecessary columns and duplicates are removed. The dataset is prepared by ensuring consistent formatting and appropriate data types for categorical and numerical variables.
   
2. **Feature Engineering**: 
   - New features like `time_of_day` (based on ad exposure time) and `ads_intensity` (low, medium, high exposure to ads) are added to help segment and analyze customer behavior.
   
3. **Descriptive and Visual Analysis**:
   - Various visualizations, including bar plots and box plots, are created to explore the relationship between test groups, time of day, and conversion rates.
   
4. **A/B Test Setup**:
   - Group sizes and conversion rates are calculated for both the control and treatment groups.
   
5. **Statistical Testing**:
   - A **chi-square test** is performed to determine if the difference in conversion rates between the control and treatment groups is statistically significant. The result suggests rejecting the null hypothesis, indicating a significant difference in conversion rates.

6. **Effect Size**:
   - **Cohen's h** is calculated to measure the magnitude of the effect, which is determined to be a large effect (0.6333). This suggests that the observed difference is both statistically and practically significant.

7. **Power Analysis**:
   - Power analysis shows that the test has sufficient statistical power (1.0000), meaning the sample size is large enough to detect even small differences in conversion rates.

#### Key Insights:
- **Group Sizes and Conversion Rates**:
   - The control group (ad) has **36,746** observations with a conversion rate of **27.3%**.
   - The treatment group (psa) has **7,732** observations with a significantly lower conversion rate of **5.34%**.
   
- **Chi-square Test**:
   - The chi-square test yields a **chi2 statistic of 1713.9967** and a **p-value of 0.0000**, indicating a statistically significant difference in conversion rates between the two groups.

- **Effect Size**:
   - The **effect size (Cohen's h)** is calculated to be **0.6333**, which is considered a large effect, suggesting a meaningful difference between the control and treatment groups.

- **Power Analysis**:
   - The power of the test is **1.0000**, meaning that the test is highly reliable, and the sample size was sufficient to detect a significant difference.

#### Business Recommendations:
- **Adopt or scale up the marketing strategy** used in the control group ("ad"), which has significantly outperformed the treatment group ("psa") in terms of conversion rates.
- The **large effect size** further strengthens the case for preferring the original ad strategy, as it shows a considerable impact on conversion rates.
- Further **optimization of the ad strategy** could yield even higher conversion rates, and additional A/B tests can be conducted to explore other variations.

### Source

https://www.kaggle.com/datasets/khanimar/marketing-campaign-analysis-data

