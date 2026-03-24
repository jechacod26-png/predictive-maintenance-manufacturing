# predictive-maintenance-manufacturing
Random Forest model for industrial equipment failure prediction — ROC-AUC 0.98 — AI4I 2020 dataset

# 🔧 Predictive Maintenance using Machine Learning

This project focuses on predicting machine failures in a manufacturing environment using machine learning techniques.

---

## 📌 Objective

To proactively detect potential failures before they impact production, enabling a transition from reactive to predictive maintenance.

---

## 📊 Dataset

- AI4I 2020 Predictive Maintenance Dataset
- 10,000 records
- 14 features including:
  - Air temperature
  - Process temperature
  - Rotational speed
  - Torque
  - Tool wear

---

## 🧠 Approach

### 1. Exploratory Data Analysis (EDA)
- Identified class imbalance (only 3.4% failures)
- Analyzed sensor distributions
- Correlation analysis between variables

### 2. Feature Engineering (Domain-Based)
- Thermal difference (process vs air temperature)
- Mechanical power (torque × speed)
- Mechanical stress
- Combined wear indicators

### 3. Data Preprocessing
- Train/Test split (80/20)
- Feature scaling (StandardScaler)
- SMOTE applied to handle imbalance

### 4. Models Used
- Logistic Regression
- Random Forest
- Gradient Boosting

---

## 📈 Results

| Model               | ROC-AUC | Avg Precision |
|--------------------|--------|--------------|
| Logistic Regression | 0.939  | 0.416        |
| Random Forest       | 0.984  | 0.849        |
| Gradient Boosting   | 0.979  | 0.856        |

🏆 **Best model: Random Forest**

---

## 🔍 Key Insights

- Mechanical stress and power are strong predictors of failure
- Tool wear combined with load increases failure probability
- Detecting false negatives is more critical than false positives in industrial environments

---

## 🏭 Industrial Impact

- Reduce unplanned downtime
- Improve Overall Equipment Effectiveness (OEE)
- Enable predictive maintenance strategies
- Lower maintenance costs

---

## ⚙️ Deployment (Simulation)

A prediction function was developed to classify machine risk:

- 🟢 Low Risk  
- 🟡 Medium Risk  
- 🔴 High Risk  

This can be integrated into real-time monitoring systems.

---

## 🧪 Example

```python
predict_failure(
    air_temp=304,
    process_temp=313,
    rot_speed=1280,
    torque=72,
    tool_wear=230,
    type='L'
)

Technologies
Python
Pandas
Scikit-learn
Matplotlib / Seaborn

Author

Johan Chacón Dávila
Data Analyst | Manufacturing & Operations



