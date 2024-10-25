
# Shared Bike Demand Prediction Using Linear Regression

This repository contains the solution to a programming assignment for predicting shared bike demand using a multiple linear regression model. The project utilizes data from BoomBikes, a U.S.-based bike-sharing provider, to help understand demand patterns and optimize business strategies in a post-pandemic market.

## Project Motivation

BoomBikes experienced a revenue decline during the COVID-19 pandemic and aims to understand the key factors driving bike demand. This project analyzes various attributes affecting daily bike rentals, enabling BoomBikes to plan its resources better and meet future demand. By identifying the significant predictors, the company can implement targeted strategies to recover and grow.

## Problem Statement

The objective is to predict the demand for shared bikes by analyzing daily bike rental data. Key objectives include:
- Identifying significant factors that influence bike demand.
- Building a model to explain the relationship between these factors and daily bike rentals.
- Using the model to provide insights for business strategy and resource planning.

## Data Overview

The dataset includes daily records of bike rentals and associated attributes, such as:
- **Meteorological Features**: Weather, temperature, humidity, etc.
- **Temporal Features**: Season, day type (working day or holiday), and year.
- **User Data**: Casual and registered users contributing to total rentals (`cnt`).

For this assignment, `cnt` is used as the target variable representing total bike demand.

### Data Preparation
Key preparation steps:
- **Encoding Categorical Variables**: Convert integer labels in `season` and `weathersit` to categorical strings.
- **Feature Selection**: Retain `yr` (year) as a potential predictor due to the trend of increasing demand.

### Dataset
The dataset and data dictionary can be found in the `/data` folder.

## Approach

1. **Data Preprocessing**: Prepare and clean data by handling missing values, encoding categorical features, and standardizing continuous variables.
2. **Model Building**: Using multiple linear regression to predict the demand (`cnt`) based on available predictors.
3. **Evaluation**: Assess model performance using metrics such as R-squared and residual analysis to check model fit.

## Model Evaluation

The model performance on the test set is evaluated using the R-squared score. The following code snippet is used to calculate it:

```python
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
```

### Evaluation Metrics:
- **R-squared Score**: Measures how well the independent variables explain the variance in bike demand.
- **Residual Analysis**: Ensures that errors are normally distributed, suggesting a good model fit.

## Repository Structure

- `Bike_Sharing_Demand_Prediction.ipynb`: Jupyter Notebook with full model-building workflow.
- `data/`: Contains the dataset and data dictionary.
- `subjective_questions.pdf`: Responses to additional questions on linear regression concepts.
- `README.md`: Project documentation (this file).

## Getting Started

### Prerequisites
Install required packages using:
```bash
pip install -r requirements.txt
```

### Running the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/username/repo-name.git
   cd repo-name
   ```
2. Open and run `Bike_Sharing_Demand_Prediction.ipynb` in Jupyter Notebook.

## Insights & Recommendations

The insights derived from the model will assist BoomBikes in understanding demand trends and guide decisions for fleet management, pricing, and marketing to meet customer expectations post-lockdown.
