# 💧 Water Potability Prediction Using Machine Learning

## Project Overview
This project analyzes and predicts **water potability** using machine learning models.  
The goal is to determine whether water is safe for consumption based on **physical and chemical properties** like pH, hardness, and other indicators.  

The project demonstrates a complete ML pipeline including **data preprocessing, exploratory data analysis (EDA), feature selection, model training, threshold tuning, and evaluation**.

---

## Dataset
- **Source:** Water Potability Dataset  
- **Size:** 3,276 samples  
- **Features:**

| Feature | Description |
|---------|-------------|
| pH | Water pH level |
| Hardness | Total hardness |
| Solids | Total dissolved solids |
| Chloramines | Chloramines concentration |
| Sulfate | Sulfate concentration |
| Conductivity | Electrical conductivity |
| Organic_carbon | Organic carbon content |
| Trihalomethanes | Trihalomethanes concentration |
| Turbidity | Turbidity level |
| Potability | Target variable: 0 = Not Potable, 1 = Potable |

- **Missing values** handled by replacing with column mean values.

---

## Methodology

### 1. Data Preprocessing
- Replaced missing values with column means.  
- Scaled features using `StandardScaler`.  
- Split data into **training (70%)** and **testing (30%)** sets.

### 2. Exploratory Data Analysis (EDA)
- Distribution plots and KDE plots to compare **potable vs non-potable water**.  
- Correlation heatmaps to identify feature relationships.  
- Bar plots and pie charts to visualize class distribution.

### 3. Feature Selection
- Used **Recursive Feature Elimination (RFE)** with Logistic Regression to select the most impactful features.

### 4. Machine Learning Models
Tested and tuned the following models, including threshold adjustments:  
- Logistic Regression  
- Random Forest Classifier  
- K-Nearest Neighbors (KNN)  
- Support Vector Machine (SVM)  
- XGBoost Classifier  

### 5. Evaluation Metrics
- **Accuracy**  
- **Confusion Matrix**  
- **Classification Report** (Precision, Recall, F1-score)  
- Visualized results using **heatmaps** for easier interpretation.

---

## Results
- **Best performance** achieved using **Random Forest** and **XGBoost** after threshold tuning.  
- Models provide insights into **how different water properties impact potability**.  
- Confusion matrices visualize correct and incorrect predictions for potable vs non-potable water.  

---

## Technologies Used
- **Python 3**  
- **Libraries:** pandas, numpy, matplotlib, seaborn, plotly, scikit-learn, xgboost  
- **Google Colab/Jupyter Notebook** for execution  

---

## How to Run
1. Clone the repository:  
```bash
git clone <repository_link>
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Run the notebook/script:

bash
Copy code
jupyter notebook water_potability_analysis.ipynb
Conclusion
This project demonstrates a complete ML pipeline from data preprocessing to model evaluation for predicting water potability.
It can assist in real-world water quality monitoring and provides a foundation for further research using advanced models or feature engineering.
