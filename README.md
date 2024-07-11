# Credit Scoring Analysis

## Project Introduction
In this project, the task is to prepare a report for the credit division of a bank focusing on the impact of customers' marital status and number of children on the probability of defaulting on loans. The bank has provided extensive data on customer creditworthiness. Credit assessment is vital for evaluating the ability of borrowers to repay their loans.

## Steps of the Project
1. **Data Exploration**
2. **Data Preprocessing**
3. **Data Categorization**
4. **Conclusion**

## Data Description
- **children**: Number of children in the family.
- **days_employed**: Duration of employment.
- **dob_years**: Age of the customer.
- **education**: Level of education.
- **education_id**: Identifier for education level.
- **family_status**: Marital status.
- **family_status_id**: Identifier for marital status.
- **gender**: Gender of the customer.
- **income_type**: Type of income.
- **debt**: Whether the customer has ever defaulted on a loan.
- **total_income**: Monthly income.
- **purpose**: Purpose of the loan.

This project aims to provide insights into factors influencing credit risk using real-world data that may contain outdated information or inaccuracies, reflecting common challenges in data management scenarios.

## Summary
In this project, given the data of historical performance of creditors and its following information. During data understanding we found that:

- Missing values were found in columns 'days_employed' and 'total_income'.
- The 'days_employed' column had unrealistic values.
- Redundancy was found in the column 'purpose'.
- Unrealistic values were present in the column 'children'.
- There was uncategorized data.

So some adjustments have been made:

- Used averages to fill missing values in 'days_employed' and 'total_income'. For 'days_employed', we also used absolute values to handle negative values and replaced unrealistic values by subtracting 'dob_years' with 18 (the start age of legally working).
- Categorized 'total_income' based on 'age_category' and filled missing values with the average value from each age category.
- Replaced redundant values in 'purpose' using the replace function.
- Replaced unrealistic values in 'children': -1 with 1 and 20 with 2, as negative children and such high values are unrealistic.
- Categorized data in columns 'income', 'children', 'days_employed'.

## Conclusion
The conclusion from the data analysis is:

- Big families demonstrate the highest default rates, notably for weddings (14.29%) and house construction (12.50%), indicating higher financial strain in these scenarios.
- Average families show significant default risks, particularly for vehicle ownership (12.05%) and education (11.24%) loans.
- Single-child families exhibit moderate default rates ranging from 7.86% to 10.68% across different loan purposes.
- Childless families generally exhibit lower default rates, ranging from 5.87% to 8.67%.
- Very big families show no defaults across all recorded purposes, possibly due to a smaller sample size or unique financial stability.

These findings underscore the critical role of family dynamics and loan purpose in evaluating credit risk and informing prudent lending practices.
