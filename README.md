# Marketing A/B Testing Analysis

## Overview

This project analyzes a marketing campaign's performance through A/B testing, comparing two different groups exposed to different ad strategies to measure their impact on customer conversion rates. The project evaluates the conversion rates between the control (ad) and treatment (psa) groups, uses statistical tests to determine significance, and calculates effect sizes and power for robust business recommendations.

## Data Description

The dataset contains the following columns:

- Unnamed: 0: An index column.
- user id: Unique identifier for each user.
- test group: Indicates the group (either 'ad' or 'psa') to which the user was assigned.
- converted: A boolean indicating whether the user converted (1) or not (0).
- total ads: The total number of ads viewed by the user.
- most ads day: The day when the user saw the most ads.
- most ads hour: The hour during which the user saw the most ads.

The dataset consists of 588,101 entries.

##### Analysis Steps:

1. Data Extraction: Extract the dataset from the ZIP file and load it into a pandas DataFrame.
2. Data Inspection: Check the basic information, summary statistics, and unique values in categorical columns.
3. Data Cleaning:
- Remove unnecessary columns.
- Handle missing values.
- Remove duplicates.
- Correct data types.
- Ensure consistent formatting in categorical columns.
4. Feature Engineering: Create new features such as time_of_day, is_weekend, and ads_intensity.
Visualization:
- Plot distribution of conversion rates.
- Compare conversion rates across groups.
- Analyze the impact of time of day and total ads on conversion rates.
5. A/B Testing:
- Perform a chi-square test to compare conversion rates between test groups.
- Calculate conversion rates and effect size.
7. Sensitivity Analysis: Assess the power of the A/B test and calculate Cohen's h effect size.

#### Results:

Group Sizes:

- Group 'ad': 564,577 users
- Group 'psa': 23,524 users

Conversion Rates:

- Group 'ad': 0.0255
- Group 'psa': 0.0179

Chi-square Test Results:

- Chi2 Statistic: 54.0058
- P-value: 0.0000
- Conclusion: Reject the null hypothesis. There is a significant difference in conversion rates between the groups.

Effect Size (Cohen's h): 0.0530

#### Key Insights:

- The observed difference in conversion rates between the control group ('ad') and treatment group ('psa') is statistically significant but has a small practical effect size.
- Recommendations include focusing on the marketing strategy associated with the 'ad' group, while considering further optimization opportunities for the 'psa' group.

#### Source:

