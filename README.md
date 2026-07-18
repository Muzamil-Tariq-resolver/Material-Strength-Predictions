# Physics-Informed Concrete Strength Prediction

Machine Learning + Physics-Guided Approach for Predicting Concrete Compressive Strength

---

# Project Overview

Concrete compressive strength is a critical factor in civil engineering, determining the durability and safety of structures. Traditional empirical methods are limited in capturing nonlinear interactions between material composition and curing conditions.

This project develops a **Physics-Informed Machine Learning model** to predict concrete compressive strength by combining:

- Material science principles  
- Physics-informed feature engineering  
- Machine learning models  
- Data-driven optimization  

The objective is to improve both prediction accuracy and engineering interpretability, enabling better mix design decisions.

---

# Problem Statement

Predicting concrete strength is challenging because:

- Material components interact non-linearly  
- Strength development depends on curing time  
- Traditional formulas oversimplify real-world behavior  
- Experimental testing is expensive and time-consuming  

The goal is to build an intelligent system that can:

- Accurately predict compressive strength (MPa)  
- Capture physics-based relationships in concrete mixtures  
- Identify optimal material compositions  
- Reduce dependency on lab testing  
- Improve construction planning and safety decisions  

---

# Databricks Model Integration

This project includes deployment and integration using Databricks SQL Warehouse.

## Dataset Description
The dataset contains real-world concrete samples capturing material composition and curing parameters used in construction.  

**Input Features:**

- Cement (kg/m³)  
- Blast Furnace Slag (kg/m³)  
- Fly Ash (kg/m³)  
- Water (kg/m³)  
- Superplasticizer (kg/m³)  
- Coarse Aggregate (kg/m³)  
- Fine Aggregate (kg/m³)  
- Age (days)  

**Target Variable:**

- Concrete Compressive Strength (MPa)  

---

## Methodology
The workflow of the project includes:

1. **Data Understanding and Inspection** – Check for missing values, duplicates, and feature distributions.  
2. **Exploratory Data Analysis (EDA)** – Analyze relationships between mix components, curing age, and strength.  
3. **Physics-Informed Feature Engineering** – Create Water–Cement Ratio (WCR), Age × WCR, and other domain-driven features.    
4. **Model Evaluation and Validation** – Use RMSE, MAE, R², and cross-validation to ensure robustness.  
5. **Interpretability and Insights** – Analyze feature importance, residuals, and identify optimal mix designs.
6. **Deploying Model** - Attaching model with DataBricks SQL Warehouse.

---

## Evaluation Metrics
Model performance was assessed using:

- **Root Mean Squared Error (RMSE)**  
- **Mean Absolute Error (MAE)**  
- **R² Score**  
- **Cross-validation R²** for overfitting detection  

---

## Physics-Informed Insights
Key findings connecting ML results to concrete physics:

- **Water–Cement Ratio (WCR)**: Main predictor of strength.  
- **Age vs Strength**: Non-linear growth; rapid early strength gain slows over time.  
- **Material Substitutions**: Slag improves strength; Fly ash had minimal effect in this dataset.  
- **Feature Importance**: Identifies components that most affect strength.  
- **Optimal Mix Design**: Cement, slag, water, and superplasticizer ratios maximizing predicted strength.

---

## Best Mix Design (Predicted Strength)

| Component / Parameter        | Value | Unit       |
|-------------------------------|-------|------------|
| Cement                        | 390   | kg/m³      |
| Blast Furnace Slag            | 189   | kg/m³      |
| Fly Ash                        | 0     | kg/m³      |
| Water                         | 146   | kg/m³      |
| Superplasticizer              | 22    | kg/m³      |
| Coarse Aggregate              | 945   | kg/m³      |
| Fine Aggregate                | 756   | kg/m³      |
| Curing Age                    | 91    | days       |

