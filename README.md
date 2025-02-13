# Gully Erosion Susceptibility Mapping

This repository contains the data, code, and scripts used for gully erosion susceptibility mapping as described in the associated study. The study involves spatial modeling, data fusion, and evaluation of machine learning methods for predicting gully erosion susceptibility.

## Study Overview
This study includes five main steps:

1. **Creating a Spatial Database**:
   - A spatial database was created, including a gully erosion inventory map and conditioning factors extracted from two data sources.
   - The data was split into training (70%) and testing (30%) datasets.

2. **Examining Factor Importance**:
   - The importance of conditioning factors from the two datasets was examined using Random Forest (RF).

3. **Spatial Modeling**:
   - Gully erosion susceptibility was modeled using two machine learning methods: Random Forest (RF) and XGBoost.

4. **Data Fusion**:
   - Data fusion was implemented at both the data and decision levels using Logistic Regression (LR) and Dempster-Shafer methods in four scenarios:
     - **Scenario 1**: No fusion.
     - **Scenario 2**: Data-level fusion.
     - **Scenario 3**: Decision-level fusion.
     - **Scenario 4**: Data- and decision-level fusion.

5. **Evaluation**:
   - The performance of RF, XGBoost, and the generated Gully Erosion Susceptibility Maps (GESMs) was evaluated using RMSE, R², and AUC metrics.

---

## Repository Structure
The repository is organized as follows:
```
Gully-Erosion-Susceptibility-Mapping/
├── Data/ # Folder containing datasets
│ ├── Gully_train.csv # Training dataset (70% of data)
│ ├── Gully_test.csv # Testing dataset (30% of data)
│ ├── SA_gully.csv # Dataset for the entire study area
│ └── SA_Fused.csv # Fused dataset for the entire study area
├── Google earth engine scripts/ # Google Earth Engine scripts for data fusion
├── Python Script/ # Python code for spatial modeling
└── README.md
```
---

## Data Description
The data used in this study can be found in the `data/` folder:
- **Gully_train.csv**:
  - Contains 16 feature columns and 1 target column named `gully` using the first dataset.
- **Gully_train_fused.csv**:
  - Contains 16 feature columns and 1 target column named `gully` using fused dataset.
- **SA_gully.csv**:
  - Dataset for the entire study area, used to generate gully erosion susceptibility maps.
- **SA_Fused.csv**:
  - Fused dataset for the entire study area.

---

## Code and Scripts
### Python Scripts
- The spatial models (RF and XGBoost) were implemented in Google Colab.
- The Python code can be found in the `python_scripts/` folder.

### Google Earth Engine Scripts
- The `.js` scripts for fusing the two datasets can be found in the `Google earth engine scripts/` folder.
---
