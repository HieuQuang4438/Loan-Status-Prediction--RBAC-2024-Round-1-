# Business Context
Company A is a financial institution that provides personal loan products. At present, loan approvals are done manually, and the company wants to streamline this process by automating it. To achieve this, they are gathering data on loan approvals from the previous year. The aim is to extract valuable insights and establish rules from this dataset that can be used to automate the loan approval process.
# Business Questions
#### Question 1: 
Visualize the following and give description (maximum 100 words for all three factors).
- CIBIL Score distribution between approved and rejected loans
- Education distribution between approved and rejected loans
- Income distribution between approved and rejected loans
#### Question 2:
Visualize the relationship between income and loan amount for approved loans. Do you think the loan amount is directly proportional to the income level? Why or why not? (maximum 150 words)
#### Question 3: 
If you were to include one more factor to predict loan outcomes, what specific factor would you choose to add, and what is the rationale behind this choice? (maximum 100 words)
# Dataset Description
|**Variable**|**Description**|
|-|-|
|loan id|Unique ID for each loan application|
|no of dependents|Number of dependents of the applicant|
|education|Applicant's education level|
|self employed|Whether the applicant is self-employed|
|income annum|Annual income of the applicant|
|loan amount|Amount of the loan requested|
|loan term|Term of the loan in months|
|cibil_score|Applicant's CIBIL score (credit score)|
|residential_asset_value|Values of residential asset owned by the applicant|
|commercial_asset_value|Values of commercial asset owned by the applicant|
|luxury_asset_values|Values of luxury asset owned by the applicant|
|bank_asset_values|Values of bank asset owned by the applicant|
|loan_status|Whether the loan was approved or rejected|

# Final Products
1. [Report](./APT._Round_1_RBAC_2024.pdf)
2. [Notebook](./APT._Round_1_RBAC_2024.ipynb)
### Question 3
#### Approach:
We will create new features based on existing data to enhance the predictive power of our models:
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM
- Suport Vector Classifier

Then we assess our models to define the best model and deploy "Feature Importance" function to define the best features for each model.
#### Outcome:
The Decision Tree, Random Forest, Gradient Boosting, XGBoost, and LightGBM models all show exceptional performance, with high accuracy (around 99.5%) and F1 scores (around 0.9940). These models demonstrate that they can effectively classify the target variable without significant error.

Based on the performance of 5 best models, in addition to the "cibil_score" feature that brings the best efficiency in prediction, you can consider the new feature "loan_to_income_ratio".

The loan_to_income_ratio feature, calculated as the ratio of loan_amount to income_annum:
- A high loan_to_income_ratio suggests that a large part of the applicant’s income goes
towards the loan, indicating a higher debt burden and potentially greater financial strain.
- Lenders often use this ratio to assess an applicant’s ability to manage loan payments relative
to their income. Borrowers with a lower loan_to_income_ratio typically have more
disposable income, making them less likely to default, while a higher ratio may indicate
higher risk.