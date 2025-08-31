## Credit Decisioning

This project demonstrates a full-stack data science workflow for credit risk modeling, moving beyond traditional statistical metrics to a business-centric, profit-maximized approach. The final output is an interactive Streamlit dashboard designed for risk analysts and lending managers.

# Project Overview
In retail finance, credit decisioning models are often optimized on statistical metrics like AUC or the KS-statistic. While useful, these metrics are "business-blind"—they don't account for the financial reality that different incorrect decisions have different costs.

This project solves that problem by:

Building a robust default prediction model using a realistic, synthetically generated dataset.

Optimizing the model's hyperparameters directly for net profit using Optuna, based on user-defined financial assumptions.

Deploying the model into an interactive Streamlit dashboard that allows for live scoring, decision explainability with SHAP, and powerful business impact simulations.

The result is a tool that bridges the gap between data science and business strategy, enabling stakeholders to make data-driven decisions that are directly aligned with financial outcomes.

# Key Features

End-to-End Pipeline: Includes scripts for data generation (test.py), a complete ETL, feature engineering, and training pipeline (model.py), and a user-facing dashboard (dashboard.py).

Profit-Maximized Hyperparameter Tuning: Uses Optuna to tune the LightGBM model's hyperparameters, maximizing a custom profit function instead of a generic statistical metric.

Interactive Business Simulation: A Streamlit dashboard allows users to adjust financial assumptions (interest income rate, cost of default) and instantly see the impact on the optimal decision threshold and overall portfolio profitability.

Features importance: Integrates SHAP to generate waterfall plots for every prediction, making the model's decisions transparent and auditable.

Automated Insights with Generative AI: Uses the Google Gemini API to provide natural language summaries and answer user questions about the dashboard's metrics.

# Technical Stack

Data Generation & Storage: Python, Faker, MySQL

Modeling & Data Science: Pandas, NumPy, Scikit-learn, LightGBM, Optuna (for tuning), SHAP (for explainability)

Dashboard & UI: Streamlit, Plotly

Generative AI: Google Gemini API

# Core Concepts Demonstrated

This project is a practical application of several key concepts in retail finance and data science:

Predictive Modeling: Building a classifier to predict a binary outcome (loan default).

Profit Maximization: Shifting model optimization from statistical purity to business value.

Model Calibration: Using Isotonic Regression to ensure predicted probabilities are reliable.

Portfolio Analysis: Performing Cohort and Roll Rate analysis to monitor portfolio health over time.

Explainable AI (XAI): Making "black box" models transparent and understandable to business users.Core Retail Finance Analytics: The project includes advanced SQL queries (queries.py) for performing Cohort Analysis and calculating Roll Rates, demonstrating a deep understanding of portfolio management metrics.

