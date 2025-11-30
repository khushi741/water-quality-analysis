💧 Water Potability Prediction Using Machine Learning
Project Overview

This project analyzes and predicts water potability using machine learning models. The goal is to determine whether water is safe for consumption based on physical and chemical properties like pH, hardness, and other indicators.

This project demonstrates data preprocessing, exploratory data analysis (EDA), feature selection, model training, threshold tuning, and evaluation.

Dataset

Source: Water Potability Dataset

Size: 3,276 samples

Features:

Feature	Description
pH	Water pH level
Hardness	Total hardness
Solids	Total dissolved solids
Chloramines	Chloramines concentration
Sulfate	Sulfate concentration
Conductivity	Electrical conductivity
Organic_carbon	Organic carbon content
Trihalomethanes	Trihalomethanes concentration
Turbidity	Turbidity level
Potability	Target variable: 0 = Not Potable, 1 = Potable

Missing values handled by replacing with mean of respective columns.

Methodology
1. Data Preprocessing

Missing values replaced with column means.

Data scaled using StandardScaler.

Split into training (70%) and testing (30%) sets.

2. Exploratory Data Analysis (EDA)

Distribution plots and KDE plots to compare potable vs non-potable water.

Correlation heatmaps to check feature relationships.

Bar plots and pie charts for class distribution.

3. Feature Selection

Used Recursive Feature Elimination (RFE) with Logistic Regression to select the most impactful features.

4. Machine Learning Models

Tested and tuned the following models with threshold adjustments:

Logistic Regression

Random Forest Classifier

K-Nearest Neighbors (KNN)

Support Vector Machine (SVM)

XGBoost Classifier

5. Evaluation Metrics

Accuracy

Confusion Matrix

Classification Report (Precision, Recall, F1-score)

Visualized using heatmaps for easy interpretation.

Results

Achieved best performance using Random Forest and XGBoost after threshold tuning.

Models provide insights on how different water properties impact potability.

Confusion matrices visualize correct and incorrect predictions for potable vs non-potable water.

Technologies Used

Python 3

Libraries: pandas, numpy, matplotlib, seaborn, plotly, scikit-learn, xgboost

How to Run

Clone the repository:

git clone <your-repo-url>


Install dependencies:

pip install -r requirements.txt


Run the notebook/script:

jupyter notebook water_potability_analysis.ipynb

Conclusion

This project demonstrates a complete ML pipeline from data preprocessing to model evaluation for predicting water potability. It can help in real-world water quality monitoring and provides a foundation for further research using more advanced models or feature engineering.

