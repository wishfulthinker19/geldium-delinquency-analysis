# Geldium Delinquency Risk Analysis

Analysis and strategy work from Tata's GenAI-Powered Data Analytics job simulation (Forage): predicting credit delinquency for a fictional lender, Geldium, and recommending how to act on it.

## The problem
Which customers are at risk of delinquency, and how should Collections respond fairly and effectively?

## Data
500 customers, 19 fields (income, credit score, credit utilization, missed payments, 6-month payment history and more). 16% of customers are delinquent. The raw dataset is not included here.

## Key findings
- **Data quality:** missing values in Income (39), Loan_Balance (29) and Credit_Score (2); inconsistent employment labels; 4 customers with credit utilization above 100%.
- **Weak signal:** every numeric correlation with delinquency was below 0.06. A quick baseline test scored AUC of about 0.45 for logistic regression (0.50 is chance), and complex models did no better.
- **Segments to watch (not statistically significant):** customers using 30%+ of their credit (16.8% delinquent vs 12.0%), business cardholders (21.3% vs 14.5%) and unemployed customers (19.4% vs 15.2%).

## Recommendation
Don't deploy on this data. Run a randomised 6-month outreach pilot for customers at 30%+ utilization, with a comparison group, and scale only if the model reaches AUC of 0.70 or more, passes fairness checks and reduces delinquency.

## Responsible AI
Age and Location excluded from decisions, fairness checks by group, plain-language explanations for every score, human review of anything that changes a customer's terms.

## Files
- `reports/`: EDA report, predictive model plan, business summary report
- `presentation/`: executive deck on an AI-powered collections system

## Tools
Python, Excel, logistic regression (conceptual model plan)
