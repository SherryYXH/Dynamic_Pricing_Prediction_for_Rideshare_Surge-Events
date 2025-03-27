# Surge Pricing Prediction in Rideshare Services

![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/surge-pricing-prediction)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📖 Project Overview
This project analyzes the drivers of surge pricing in rideshare platforms and builds machine learning models to predict surge pricing events. Using real-world data from Boston-area rideshare operations, we explore:
- Key factors influencing surge pricing
- Statistical patterns in ride costs and demand
- Predictive performance of three ML models

**Key Insight**: Gradient Boosting emerged as the best predictor with 98% accuracy and 0.92 ROC-AUC score.

## 📊 Key Findings
- **Surge Pricing Impact**: Rides during surge periods show 150-200% price increases (median $25-30 vs $10-15)
- **Critical Features**:
  - Ride price (most significant predictor)
  - Distance traveled
  - Ride provider (Uber vs Lyft)
  - Geographic patterns
  - Weather conditions
- **Model Comparison**:
  | Model | Accuracy | Precision | Recall | ROC-AUC |
  |-------|----------|-----------|--------|---------|
  | Gradient Boosting | 98% | 95% | 29% | 0.92 |
  | Random Forest | 97% | 52% | 37% | 0.91 |
  | Logistic Regression | 97% | 100% | 10% | 0.90 |

## 🛠 Technical Implementation
### Data Pipeline
```python
# Simplified data processing flow
1. Data Cleaning:
   - Remove duplicates & missing values
   - Drop non-essential columns
   - Convert datetime formats

2. Feature Engineering:
   - Extract temporal features (hour, dayofweek)
   - Encode categorical variables
   - Normalize numerical features

3. Model Training:
   - 80/20 train-test split
   - Class balancing using SMOTE
   - Hyperparameter tuning with GridSearchCV
