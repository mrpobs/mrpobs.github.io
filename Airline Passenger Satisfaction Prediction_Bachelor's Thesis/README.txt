Airline Passenger Satisfaction Prediction
Overview
This project applies predictive modeling techniques to forecast passenger satisfaction levels in the airline industry. It is built on a comprehensive dataset containing over 129,000 records across 25 variables, capturing a wide array of factors related to passenger experience.

The goal is to provide airlines with an actionable, data-driven tool to identify potential dissatisfaction in advance and improve operational decision-making.

Project developed as part of the final degree project (TFG) in the Master's in Big Data Science (MBDS) at Universidad de Navarra by:

Diego Rafael de Lemos

Leyre de la Calzada

Carmen Casado

Pablo Benavides

Dick Rogeir Lizana

Project Structure
aerolinea_db5a_mbds.py: This script performs preprocessing, exploratory analysis, imputation of missing data, variable encoding, and feature engineering to prepare the dataset for modeling.

aerolinea_db5a_modelado_mbds.py: Responsible for modeling, evaluation, and interpretation. Includes feature selection techniques (Lasso, Random Forest, RFE), dimensionality reduction (PCA), and classification model training.

Dataset
The dataset includes:

Demographics (e.g., gender, age, travel type)

Service-related ratings (e.g., wifi, food, comfort, cleanliness)

Operational metrics (e.g., delays, flight distance)

Target variable: Binary satisfaction score (1 = satisfied, 0 = neutral/dissatisfied)

All satisfaction ratings are on a scale from 0 to 5.

Objective
To build an interpretable and robust binary classification model that predicts whether a passenger will be satisfied based on their profile and travel experience.

Setup & Requirements
Run in a Python 3.10+ environment with the following packages:

bash
Copiar
Editar
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
Methodology
1. Data Preparation (aerolinea_db5a_mbds.py)
Removal of irrelevant columns

Imputation of missing values (mean/median-based)

Binary and ordinal encoding of categorical features

Exploratory data visualizations (e.g., violin plots, histograms, correlation matrix)

2. Feature Selection
Lasso Regression: Identifies key linear contributors

Random Forest Importance: Captures nonlinear influences

Recursive Feature Elimination (RFE): Selects top 5 features

PCA: Dimensionality reduction (explains 47% of variance with 2 components)

3. Modeling (aerolinea_db5a_modelado_mbds.py)
Multiple models tested (Logistic Regression, Random Forest, XGBoost)

Evaluation using confusion matrix, accuracy, precision, recall, and AUC

Final model interprets key drivers of satisfaction

Results
Key predictors include:

Online boarding

Business travel

Seat comfort

On-board service

Loyalty status

Accuracy of final models: ~85%

Insight: Most dissatisfaction stems from low ratings in WiFi, gate location, and arrival delays.

Business Value
This tool empowers airlines to:

Proactively address dissatisfaction

Personalize services for business vs leisure travelers

Prioritize investment in services with higher satisfaction impact

Increase customer retention through loyalty optimization

Limitations & Future Work
Does not yet incorporate unstructured data (e.g., social media feedback)

Uses static data; future work should include time series to capture seasonal effects

Potential expansion to multiclass satisfaction levels for finer granularity

License
This work is academic in nature and licensed under the Creative Commons Attribution-NonCommercial 4.0 International License.