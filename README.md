
# Credit Card Approval Analysis

## Executive Summary

This case study provides a comprehensive exploratory data analysis (EDA) for credit card approval data. The analysis explores key trends, customer behaviors, and potential areas for growth in the context of credit card approvals. Key insights include:

- **Expenditure as a Critical Factor** : Applicants with   higher monthly expenditures are more likely to be approved for credit cards.
-  **Impact of Derogatory Reports** : A high number of derogatory reports significantly decreases the likelihood of credit card approval.
-  **Customer Segmentation** : Clustering revealed distinct customer segments, including high-income, stable applicants (prime candidates) and high-risk groups with poor credit histories.


These insights could help the bank optimize its credit card approval process by identifying key predictors of approval and tailoring products to specific customer segments.


## Problem Statement

To support the bank’s goal of improving its credit card approval process, this analysis aims to:

- Understand key trends in customer financial behavior (e.g., income, expenditure, credit history).
- Identify variables that significantly influence credit card approval decisions.
- Segment customers into distinct groups based on their financial profiles to enable targeted marketing and risk management strategies.

## Dataset
This EDA used the CreditCard.csv dataset, which includes 1,319 observations and 12 variables. The dataset covers critical fields such as:

- **Demographics** : Age, dependents, homeownership, self-employment status.
- **Financial Behavior** : Income, monthly expenditure, ratio of - expenditure to income, number of active credit accounts.
- **Credit History** : Number of major derogatory reports, number of major credit cards held.
- **Response Variable** : Credit card approval status (card).


## Tools Used
The analysis was conducted using Python with the following libraries:

- **Pandas** : For data manipulation and cleaning.
- **Matplotlib/Seaborn** : For data visualization.
- **NumPy** : For numerical computations.
- **Scikit-learn** : For logistic regression, clustering (KMeans), and dimensionality reduction (PCA).
- **SciPy** : For statistical tests (Chi-Square, T-test, Mann-Whitney U Test).


### **Key Findings**

| **Analysis Type**         | **Variable/Cluster**                                                                 | **Finding**                                                                                                                                                                                                 | **Implications**                                                                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Demographic Analysis**   | **Age Groups**                                                                     | Majority of applicants fall into the age group of 20-40, with younger applicants (20-30) being a significant portion of the applicant pool.                                                                 | Younger demographics are a strong target for marketing efforts. Tailored products (e.g., entry-level credit cards) could attract this group.                                                                    |
|                            | **Homeownership**                                                                  | Homeowners are more likely to be approved for credit cards compared to non-homeowners.                                                                                                                     | Homeownership is a strong positive factor in credit card approval decisions. Marketing strategies should emphasize this demographic.                                                                            |
|                            | **Self-Employment**                                                                | Self-employed individuals have a marginally lower approval rate compared to non-self-employed individuals.                                                                                                | Banks may need to exercise caution when dealing with self-employed applicants, as they might be perceived as higher risk.                                                                                       |
| **Financial Behavior**     | **Expenditure**                                                                    | Higher monthly expenditures strongly correlate with credit card approval. Applicants with higher spending patterns are more likely to be approved.                                                          | Expenditure is a critical predictor of credit card approval. Banks should focus on applicants with proven spending patterns.                                                                                    |
|                            | **Income**                                                                         | Surprisingly, income has a slightly negative coefficient in the logistic regression model, indicating that higher income alone does not strongly influence approval.                                         | Income alone is less influential than spending behavior. Banks should prioritize applicants who actively utilize credit rather than those with high income but low expenditure.                                   |
|                            | **Derogatory Reports**                                                             | A high number of derogatory reports significantly decreases the likelihood of credit card approval.                                                                                                        | Derogatory reports are a clear indicator of poor credit behavior. Banks should reject applications from individuals with multiple derogatory reports or implement stricter scrutiny for this group.             |
|                            | **Dependents**                                                                     | The presence of dependents negatively impacts credit card approval. Applicants with more dependents are less likely to be approved.                                                                        | Applicants with many dependents may be perceived as having higher financial responsibilities. Banks may view this as a risk factor and should monitor such cases carefully.                                       |
| **Customer Segmentation**  | **Cluster 0 & 1**                                                                  | Stable, higher-income individuals with moderate expenditure and low derogatory reports—prime candidates for credit card approvals.                                                                         | These clusters represent financially stable customers. Banks should prioritize them for premium credit card offers.                                                                                             |
|                            | **Cluster 2**                                                                      | High-risk group with very high derogatory reports, low expenditure, and moderate income—likely to be rejected.                                                                                            | This cluster represents high-risk individuals. Banks should either reject applications or offer secured credit products with additional scrutiny.                                                                |
|                            | **Cluster 3 & 4**                                                                  | Younger, low-income individuals with limited credit history and fewer active accounts—potential targets for entry-level or secured credit cards.                                                           | Banks should target these clusters with entry-level products to help them build credit responsibly while monitoring their spending and repayment patterns.                                                       |
|                            | **Cluster 5**                                                                      | Young individuals with high expenditure and moderate income—profitable but require monitoring for overextension risks.                                                                                     | While these individuals are highly profitable due to their spending, banks should closely monitor them for potential overextension risks.                                                                       |

---


2. **Financial Behavior Trends**

- **Finding** : Expenditure is the most critical predictor of credit card approval. Higher monthly expenditures correlate strongly with approval, while the number of derogatory reports has a strong negative impact.

- **Implications** : Banks should focus on applicants with proven spending patterns and low derogatory reports. High-income individuals with low expenditure may not be as appealing due to lower profitability.

3. **Customer Segmentation**

- **Findings** : Clustering identified six distinct customer segments:
    1. **Cluster 0 & 1** : Stable, high-income individuals with
    moderate expenditure and low derogatory reports—prime
    candidates for premium credit cards.

    2. **Cluster 2** : High-risk group with very high
    derogatory reports and low expenditure—likely to be
    rejected.

    3. **Cluster 3 & 4** : Younger, low-income individuals with
    limited credit history—potential targets for entry-level or
    secured credit cards.

    4. **Cluster 5** : Young individuals with high expenditure  
    and moderate income—profitable but require monitoring for 
    overextension risks.


-  **Implications** : Tailored strategies can be implemented for each segment, such as offering premium products to stable clusters and mitigating risks for high-risk groups.

## Recommendations

- **Marketing** : Focus on younger demographics (20-40) and homeowners, as they are more likely to be approved for credit cards.
- **Risk Management** : Implement stricter scrutiny for applicants with high derogatory reports (Cluster 2) and monitor high-expenditure individuals (Cluster 5) for overextension risks.
- **Product Development** : Develop entry-level or secured credit cards for younger, low-income applicants (Clusters 3 & 4) to help them build credit responsibly.


## Impact Analysis
Implementing these recommendations could lead to:

- **Revenue Growth** : Targeted marketing efforts toward stable, high-income applicants (Clusters 0 & 1) could increase approval rates and profitability.

- **Enhanced Risk Management** : Identifying and mitigating risks for high-risk groups (Cluster 2) can reduce default rates.
- **Improved Customer Experience** : Offering tailored products (e.g., entry-level cards for younger applicants) can enhance customer satisfaction and loyalty.

## Conclusion
This EDA highlighted key patterns and actionable insights that can help the bank optimize its credit card approval process. By leveraging demographic, financial, and behavioral data, the bank can refine its strategies to better align with customer needs and achieve its business goals.

