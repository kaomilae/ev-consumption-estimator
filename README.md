#  EV Energy Consumption Predictor

> Predicting electric vehicle energy consumption using Machine Learning  combining driving behavior, vehicle state, and environmental conditions.

---

##  About the Project

This project applies **XGBoost Regression** to predict how much energy (kWh) an electric vehicle consumes, based on real-world driving variables. It was built with a focus not only on accuracy, but also on **interpretability** and **physical meaningfulness**  ensuring the model makes sense from an automotive engineering perspective.

---

##  Model & Evaluation

| Component | Details |
|---|---|
| **Algorithm** | XGBoost Regressor |
| **Validation strategy** | Cross-validation + holdout set |

### Results

| Metric | Value |
|---|---|
| R (holdout) | **0.93** |
| Mean R (CV) | **0.936** |
| MAE | **0.45 kWh** |
| RMSE | **0.56 kWh** |

 Stable across all folds  
 No signs of overfitting  
 Strong generalization performance  

---

##  Model Explainability (SHAP)

SHAP values were used to interpret the model's predictions. The most influential features were:

1.  **Speed**  most important driver of energy consumption
2.  **Distance traveled**
3.  **Battery state of charge (SoC)**
4.  **Environmental conditions**  humidity, temperature, road slope

This confirms the model is not only accurate, but also **physically meaningful** and aligned with real-world automotive behavior.

---

##  Dataset

This project uses the **EV Energy Consumption Dataset** from Kaggle.

| | |
|---|---|
| **Source** | [EV Energy Consumption Dataset](https://www.kaggle.com/datasets/ziya07/ev-energy-consumption-dataset) |
| **Author** | ziya07 |
| **Platform** | Kaggle |

>  The dataset is **not included** in this repository. Download it directly from Kaggle and place it in the `data/` folder.

---

##  Project Structure

```
ev-consumption-estimator/

 data/                  # Raw and processed datasets
 notebooks/             # Exploratory analysis and model training
 models/                # Saved model files
 src/                   # Source code (preprocessing, training, evaluation)
 reports/               # SHAP plots, evaluation charts
 README.md
```

---

##  Key Takeaway

EV energy consumption is a **highly nonlinear problem** influenced by multiple interacting variables. This project integrates:

-  **Machine Learning**  XGBoost for nonlinear regression
-  **Model validation**  Cross-validation for robust performance estimates
-  **Explainability**  SHAP for feature importance and interpretability
-  **Automotive domain knowledge**  physically grounded feature selection

---

##  Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![XGBoost](https://img.shields.io/badge/XGBoost-Regressor-orange)
![SHAP](https://img.shields.io/badge/SHAP-Explainability-green)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Validation-yellowgreen?logo=scikit-learn)

---

##  Author

**kaomilae**  
Production Controller | ML enthusiast | Automotive & EV systems  

 *Always learning and exploring the intersection between AI and automotive systems.*
