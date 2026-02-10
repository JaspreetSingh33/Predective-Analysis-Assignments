# Synthetic Data Generation and Classification Using SIR Simulation

This repository contains an academic implementation focused on generating synthetic data through epidemiological simulation and applying machine learning techniques for outbreak classification. The data is produced using the classical SIR (Susceptible–Infected–Recovered) model and analyzed using multiple supervised learning algorithms.

---

## Simulation Framework

### SIR Model Description

The SIR model divides a population into three compartments that evolve over time:

- **Susceptible (S):** Individuals vulnerable to infection  
- **Infected (I):** Currently infected individuals  
- **Recovered (R):** Individuals who have recovered and developed immunity  

The transitions between these compartments are governed by differential equations.

---

## Parameter Configuration

For each simulation, parameters were randomly sampled within the following bounds:

| Parameter | Description | Range |
|---------|-------------|-------|
| β (beta) | Transmission rate | 0.1 – 1.5 |
| γ (gamma) | Recovery rate | 0.05 – 0.5 |
| N | Population size | 500 – 5000 |
| I₀ | Initial infected individuals | 1 – 50 |
| Duration | Simulation days | 80 – 200 |

---

## Dataset Generation

A total of **1000 independent simulations** were executed. From each simulation, the following attributes were extracted:

- Peak infected proportion  
- Time to reach peak infection  
- Final recovered proportion  
- Basic reproduction number (R₀ = β / γ)  

The generated dataset is saved as:

```
sim.csv
```

---

## Target Variable Definition

Each simulation outcome was labeled for binary classification:

- **1 (Severe Outbreak):** Peak infected fraction > 0.10  
- **0 (Non-Severe Outbreak):** Peak infected fraction ≤ 0.10  

---

## Data Visualization

To explore the dataset distribution, the following visualizations were produced:

- Peak infected fraction distribution  
- Class balance between severe and non-severe outbreaks  

These plots help in understanding outbreak severity patterns.

---
---

## Graphs
<img width="867" height="492" alt="Screenshot 2026-02-10 230129" src="https://github.com/user-attachments/assets/3d1760a5-7b70-4d16-b808-b67171205fc0" />
<img width="675" height="468" alt="Screenshot 2026-02-10 230144" src="https://github.com/user-attachments/assets/bc4ce198-f50d-4682-8647-1cfc2f14ee67" />

---

## Machine Learning Models Implemented

The following classification models were trained and evaluated:

- Logistic Regression  
- Random Forest  
- Gradient Boosting  
- Support Vector Classifier (SVC)  
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Multi-Layer Perceptron (MLP)  

## Model Comparison Table

<img width="1263" height="219" alt="Screenshot 2026-02-10 230302" src="https://github.com/user-attachments/assets/080351d4-53f5-475f-84f5-d064faf7dcdc" />

```
comparison.csv
```
---

## Evaluation Metrics

Model performance was assessed using:

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- ROC–AUC  

A comparative performance table summarizes the results.

---

## Best Performing Model

The **Decision Tree Classifier** demonstrated superior performance across all metrics:

- **Accuracy:** 1.00  
- **F1 Score:** 1.00  
<img width="253" height="321" alt="Screenshot 2026-02-10 230318" src="https://github.com/user-attachments/assets/fa66dc3e-e0e0-41ed-a9c1-095fab8190a9" />

---

## Author

**Jaspreet Singh**

