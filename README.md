# Hydrological Stress Prediction using TerraClimate Data (1960–2024)

## Overview

This repository contains the Python scripts developed to compute hydrological water balance, drought stress indicators, and machine learning models for predicting hydrological stress probability using TerraClimate data for the period **1960–2024**.

The workflow integrates climate raster processing and machine learning techniques to evaluate spatial patterns of water stress and identify drought-prone regions.

The methodology combines geospatial analysis with machine learning models to estimate the probability of hydrological stress across the study area.

---

## Study Objective

The main objective of this project is to:

* Compute annual **water balance** from precipitation and evapotranspiration.
* Identify **hydrological stress conditions**.
* Estimate **stress frequency and probability**.
* Generate climate summary variables.
* Train machine learning models to predict hydrological stress probability.

---

## Data Source

Climate variables were obtained from:

* **TerraClimate dataset**
* Temporal coverage: **1960–2024**
* Variables used:

  * Precipitation (PR)
  * Potential evapotranspiration (ETP)

---

## Methodological Workflow

The complete workflow implemented in this repository follows the steps below:

1. Preprocessing of climate rasters
2. Calculation of annual water balance
3. Identification of hydrological stress conditions
4. Computation of stress frequency
5. Estimation of stress probability
6. Generation of mean climatic variables
7. Extraction of spatial datasets
8. Machine learning modeling

Workflow summary:

TerraClimate PR & ETP
↓
Water Balance Calculation
↓
Hydrological Stress Detection
↓
Stress Frequency
↓
Stress Probability
↓
Mean Climate Variables
↓
Dataset Generation
↓
Machine Learning Models

---

## Repository Structure

```
hydrological-stress-ml/

scripts/
    01_water_balance.py
    02_hydrological_stress.py
    03_stress_frequency.py
    04_stress_probability.py
    05_climate_means.py
    06_extract_dataset.py

ml_models/
    random_forest.py
    gradient_boosting.py

pipeline/
    pipeline_climate_ml.py

outputs/
    generated maps and datasets

README.md
requirements.txt
```

---

## Machine Learning Models

Two machine learning models were implemented:

* Random Forest Regression
* Gradient Boosting Regression

These models were used to predict **hydrological stress probability** based on:

* Mean precipitation
* Mean evapotranspiration
* Mean water balance

Model performance was evaluated using:

* RMSE (Root Mean Square Error)
* MAE (Mean Absolute Error)
* R² (Coefficient of determination)

---

## Installation

Clone the repository:

```
git clone https://github.com/yourusername/hydrological-stress-ml.git
```

Install required libraries:

```
pip install -r requirements.txt
```

Required Python libraries:

* numpy
* pandas
* rasterio
* scikit-learn
* matplotlib

---

## Running the Pipeline

The entire preprocessing workflow can be executed using:

```
python pipeline_climate_ml.py
```

This script generates:

* Stress frequency raster
* Stress probability raster
* Mean climate rasters
* Machine learning dataset

---

## Output Products

The workflow produces the following outputs:

* Water balance maps
* Hydrological stress maps
* Stress frequency map
* Stress probability map
* Climate mean maps
* Machine learning dataset

---

## Reproducibility

All scripts were developed to ensure **full reproducibility of the analysis pipeline** from climate raster inputs to machine learning outputs.

---

## Contact

For questions or collaborations, please contact the repository author.
