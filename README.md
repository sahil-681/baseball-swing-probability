# Swing Probability Project

## Objective
The primary goal of this project is to develop a predictive model that estimates the swing probability for pitches during a baseball game. By analyzing a dataset of around 2,000,000 pitches, the model aims to provide accurate swing probability estimates for pitches in the third season, thereby aiding strategic decision-making in gameplay and player analysis.

## Data Overview
The dataset comprises information from three seasons of baseball games, including approximately 2,000,000 pitches. Key variables include:
- `season`
- `pitch_id`
- `release_speed`
- `batter`
- `pitcher`
- `description`
- `stand`
- `p_throws`
- `pitch_type`
- `balls`
- `strikes`
- `pfx_x`
- `pfx_z`
- `plate_x`
- `plate_z`
- `sz_top`
- `sz_bot`

## Methodology
### 1. Data Cleaning and Preprocessing
- Converted numeric columns to appropriate formats.
- Identified and handled missing values by removing rows with incomplete data.
- Created a target variable `swing` based on the `description` column, where non-swing descriptions were labeled as 0 and swing-related descriptions as 1.

### 2. Feature Engineering
- Engineered new features such as `ball_strike_ratio` to represent the count of balls to strikes.
- Categorized pitch types into `fastball`, `breaking`, and `offspeed` for dimensionality reduction.
- Created an interaction term between pitch type and release speed to capture combined effects.

### 3. Exploratory Data Analysis
- Visualized pitch distributions, swing probabilities, and positional data to understand patterns and relationships.
- Analyzed scatter plots and histograms to identify key features influencing swing decisions.

### 4. Model Development
- Trained multiple machine learning models including Logistic Regression, Random Forest, and XGBoost.
- Evaluated model performance using metrics such as accuracy, precision, recall, F1 score, and ROC AUC.
- Selected XGBoost as the final model due to its superior performance in predicting swing probability.

### 5. Model Evaluation
- Validated models using cross-validation techniques to ensure robustness and generalizability.
- Analyzed confusion matrices and performance metrics to interpret model effectiveness and accuracy.

## Results
- Developed a final predictive model using XGBoost, achieving an accuracy of 0.86 and an ROC AUC of 0.94.
- Generated a validation CSV file with swing probabilities for pitches in the third season, providing actionable insights for strategic gameplay decisions.

## Impact
This project leverages advanced analytics to provide a data-driven approach to understanding and predicting swing behavior. By integrating this model into a strategic framework, any baseball team can make informed decisions to enhance player performance and optimize game outcomes.
