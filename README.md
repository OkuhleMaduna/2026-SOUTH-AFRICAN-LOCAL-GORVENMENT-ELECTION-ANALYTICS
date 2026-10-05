# 2026-SOUTH-AFRICAN-LOCAL-GORVENMENT-ELECTION-ANALYTICS
TP 2 EXAM

# eThekwini 2026 Local Government Election Analytics

## Project Overview

This project develops a machine learning solution to analyse historical
election results in the eThekwini Metropolitan Municipality and estimate
selected outcomes for the 04 November 2026 Local Government Election.

The project includes a reproducible Jupyter Notebook and a Streamlit
dashboard/application.

Historical election data from 2011, 2016 and 2021 is used for data
preparation, exploratory analysis, feature engineering, machine learning
modelling, validation, evaluation and final predictions.

---

## Project Objectives

The main objectives of the project are to:

- Analyse historical election results in eThekwini.
- Examine political party voting patterns.
- Estimate party vote share for the 2026 election.
- Identify the projected leading party.
- Estimate outcomes for selected wards.
- Analyse historical voter turnout.
- Estimate voter turnout for 2026.
- Compare machine learning models.
- Present the final results through an interactive Streamlit dashboard.

---

## Dataset

The project uses three historical election datasets:

- `ETH 2011.csv` - 2011 election results
- `ETH.csv` - 2016 election results
- `ETH 2021.csv` - 2021 election results

The datasets contain information such as:

- Municipality
- Ward
- Voting District
- Voting Station
- Registered Voters
- Ballot Type
- Spoilt Votes
- Political Party
- Total Valid Votes

The 2011 dataset uses UTF-16 encoding and is loaded accordingly in the
Jupyter Notebook.

---

## Methodology

The project follows a machine learning lifecycle consisting of:

1. Problem Definition
2. Data Collection
3. Data Preparation
4. Data Understanding
5. Exploratory Data Analysis
6. Feature Engineering
7. Model Building
8. Model Evaluation
9. Model Comparison
10. Final Predictions
11. Conclusion

---

## Data Preparation

The datasets are checked and prepared by:

- Checking missing values
- Removing duplicate records
- Standardising column names
- Selecting relevant variables
- Converting numerical variables to numeric data types
- Combining the historical election datasets
- Creating election-year information

---

## Exploratory Data Analysis

Exploratory analysis is performed to identify historical patterns and trends.

The analysis includes:

- Party vote totals
- Party performance across election years
- Historical voter turnout
- Registered voters
- Ward information
- Spoilt votes
- Vote-share trends

Visualisations are used to make the historical patterns easier to interpret.

---

## Feature Engineering

The main features developed for modelling include:

- Election Year
- Party Code
- Ward Code
- Party Vote Share

Party vote share is used as the main target variable for the machine learning
model.

---

## Machine Learning Models

Two regression models are evaluated:

### Linear Regression

Linear Regression is used as a baseline model for predicting party vote share.

### Random Forest Regression

Random Forest Regression is used to capture more complex relationships in
the historical election data.

---

## Model Evaluation

The models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

The evaluation results were:

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 5.2888 | 12.2647 | 0.042 |
| Random Forest Regression | 1.2150 | 4.5013 | 0.871 |

Random Forest Regression was selected as the preferred model because it
achieved lower prediction errors and a substantially higher R² score.

---

## 2026 Election Predictions

The Random Forest model was used to estimate party vote shares for the
04 November 2026 election.

The projected leading party is:

**African National Congress (ANC)**

Estimated vote share:

**43.95%**

Other major projected party vote shares include:

- Democratic Alliance: 22.03%
- Economic Freedom Fighters: 11.19%
- Inkatha Freedom Party: 7.92%
- Independent: 6.05%

These values are model-based estimates and are not confirmed election
results.

---

## Selected Ward Predictions

Three wards were selected for the 2026 prediction analysis.

| Ward | Projected Leading Party | Predicted Vote Share |
|---|---|---:|
| Ward 59500001 | African National Congress | 75.45% |
| Ward 59500002 | African National Congress | 75.23% |
| Ward 59500003 | African National Congress | 69.24% |

---

## Voter Turnout

Historical turnout estimates were calculated using the available election
data.

| Year | Turnout |
|---|---:|
| 2011 | 59.20% |
| 2016 | 59.10% |
| 2021 | 41.53% |

A Linear Regression trend model was used to estimate 2026 voter turnout.

The estimated 2026 results are:

- Estimated registered voters: **2,074,375**
- Estimated voters: **738,557**
- Estimated turnout: **35.60%**

These are estimates based on historical trends.

---

## Streamlit Dashboard

The project includes an interactive Streamlit dashboard.

The dashboard provides the following sections:

- Overview
- Party Predictions
- Ward Predictions
- Voter Turnout
- Model Evaluation

The dashboard allows users to interactively view the historical analysis,
model results and 2026 predictions.

---

## Project Structure

```text
Election_Project/
│
├── app.py
├── election_analysis.ipynb
├── requirements.txt
├── README.md
│
├── ETH 2011.csv
├── ETH.csv
└── ETH 2021.csv
