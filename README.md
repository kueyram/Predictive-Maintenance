# Optimizing Equipment Performance through Predictive Maintenance Strategies

## Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
   - [Objectives](#objectives)
   - [Target Audience](#target-audience)
3. [Data Selection](#data-selection)
4. [Data Cleaning](#data-cleaning)
5. [Data Exploration](#data-exploration)
6. [Models Selection](#models-selection)
   - [Logistic Regression](#logistic-regression)
   - [Random Forest](#random-forest)
7. [Feature Engineering](#feature-engineering)
8. [Model Performance](#model-performance)
   - [Logistic Regression Results](#logistic-regression-results)
   - [Random Forest Results](#random-forest-results)
9. [Conclusion](#conclusion)
10. [References](#references)
11. [Installation](#installation)
12. [Usage](#usage)
13. [License](#license)

## Introduction

In manufacturing industries, unexpected equipment breakdowns can disrupt operations, leading to production delays, increased expenses, and safety risks. This project introduces a proactive predictive maintenance strategy to minimize unplanned downtime and enhance equipment reliability. Predictive maintenance forecasts potential breakdowns, allowing companies to schedule maintenance during non-critical times, ultimately cutting costs and extending equipment lifespan while ensuring worker safety.

## Project Overview

### Objectives
- Implement a predictive maintenance strategy to reduce equipment failures.
- Utilize data-driven methods to forecast breakdowns and optimize maintenance schedules.
- Enhance the reliability and safety of manufacturing operations.

### Target Audience
This project is aimed at manufacturing companies, maintenance teams, and stakeholders looking to optimize maintenance schedules and reduce equipment failures.

## Data Selection

The dataset used in this project is sourced from Kaggle, containing sensor readings, operational parameters, maintenance records, and historical failure data. Each row includes:
- Air and process temperatures
- Rotational speed
- Torque
- Tool wear
- Failure occurrence and type

## Data Cleaning

Before analysis, we checked for duplicates and missing values. The dataset was found to be clean, with no duplicates or missing values.

## Data Exploration

We created visualizations to understand the relationships within the dataset:
- **Air Temperature vs. Process Temperature:** Shows a positive correlation.
- **Histogram of Key Features:** Indicates that key features are normally distributed.
- **Distribution of Failure Types:** Identifies power and heat dissipation as primary causes of equipment failure.

## Models Selection

### Logistic Regression
Used for binary classification to predict whether equipment will fail. It estimates the probability of failure based on input features.

### Random Forest
Used for multiclass classification to predict the type of failure, combining multiple decision trees to improve prediction accuracy and robustness.

## Feature Engineering

- Removed unnecessary columns (e.g., Product ID).
- Converted temperatures from Kelvin to Fahrenheit.
- Created new features:
  - Power consumption
  - Temperature difference
  - Temperature ratio
- Scaled numerical values using MinMaxScaler.
- Created dummy variables for categorical columns.

## Model Performance

### Logistic Regression Results
- **Accuracy:** 99.6%
- **Precision:** 99.61%
- **Recall:** 99.6%
- **F1-Score:** 99.60%

### Random Forest Results
- **Accuracy:** 99.35%
- Top contributing features: Torque, Rotational speed, Tool wear, Temperature, Power consumption.

## Conclusion

Both models are effective for predicting equipment failures. Monitoring key features and utilizing both models together will create a comprehensive predictive maintenance system. Ethical considerations include data privacy and model limitations, necessitating regular updates with new sensor data.

## References

1. Breiman, L. (2001). Random Forests. Machine Learning, 5-32.
2. Gallatin, K. (2023). Machine Learning with Python. Sebastopol, CA: O'Reilly Media, Inc.
3. Hosmer, D. W. (2013). Applied Logistic Regression (3rd ed.). John Wiley & Sons.
4. Sokolova, M., & Lapalme, G. (2001). A systematic analysis of performance measures for classification tasks. Information Processing & Management, 427 - 437.

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/your-repo-name.git
```

## Requirements
1- Install required libraries

```bash
pip install -r requirements.txt
```

2- Run the project

```bash
python main.py
```

## License
This project is licensed under the MIT License.