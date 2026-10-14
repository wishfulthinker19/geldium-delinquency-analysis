# Geldium Delinquency Risk Analysis & AI Collections Strategy

**Tata GenAI Powered Data Analytics Job Simulation | Forage**

An analytical project exploring credit delinquency prediction and responsible AI-powered collections in financial services.

## Project Overview

The objective was to analyse customer financial data, identify potential delinquency risk indicators, and propose an AI-driven collections strategy for Geldium, a fictional financial institution.

## Dataset

- **500 customers**
- **19 fields**
- **16% observed delinquency rate**

Key variables included credit score, income, credit utilization, missed payments, debt-to-income ratio, and payment history.

*The raw dataset is not included in this repository.*

## Key Findings

- Identified missing values in income, loan balance, and credit score.
- Found inconsistent employment labels and credit utilization values exceeding 100%.
- A baseline test (logistic regression, random forest and gradient boosting, 5-fold cross-validation) scored AUC of about 0.40 to 0.45, which is no better than chance given the small sample. See `notebooks/baseline_model.ipynb`.
- Customers with credit utilization of 30% or more showed a higher observed delinquency rate, although the difference was not statistically significant in the reported analysis.

## Recommendations

- Validate data quality and investigate the weak predictive signal before deployment.
- Test supportive early-payment outreach through a controlled pilot.
- Evaluate model performance, customer outcomes, and fairness before scaling.
- Maintain human oversight, explainability, and responsible data practices.

## Project Deliverables

- [Reports](./reports/): EDA report, predictive modelling plan, and stakeholder recommendations.
- [Executive Presentation](./presentation/): AI-powered collections strategy.
- [Baseline Model](./notebooks/): data checks and baseline model test.

## Concepts Explored

Exploratory Data Analysis (EDA) · Predictive Analytics · Logistic Regression · Risk Assessment · Responsible AI · Business Reporting · Agentic AI Strategy

*Note: the model plan is conceptual. The baseline test in the notebook is a quick check, and the system described here is a proposal, not production-ready.*

## Key Learnings

- Data quality is essential for reliable analysis.
- Complex models do not automatically produce better predictions.
- Correlation does not establish causation.
- AI-driven financial decisions require fairness, transparency, and human oversight.

## Disclaimer

This is an educational portfolio project based on Tata's GenAI Powered Data Analytics Job Simulation hosted by Forage. Geldium is fictional. This repository is an independent learning project, not an official Tata business implementation.
