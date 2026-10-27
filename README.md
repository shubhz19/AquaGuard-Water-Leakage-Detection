# AquaGuard: Water Pipeline Leakage Detection

## Overview

AquaGuard is a machine learning project exploring water-utility sensor data to identify patterns associated with confirmed water pipeline leak events.

The project focuses on learning the complete data science workflow, including data exploration, preprocessing, model development, and evaluation.

## Objectives

- Explore water-utility sensor data.
- Investigate missing values and data quality.
- Analyze patterns in sensor-related features.
- Develop and evaluate a machine learning baseline.
- Investigate dynamic pressure sensor recordings as a potential extension.

## Project Status

**Current stage:** Exploratory Data Analysis (EDA)

Completed:
- Python environment setup.
- Initial dataset inspection.
- Target-label distribution analysis.
- Missing-value analysis.
- Timestamp validation and ordering investigation.

Planned:
- Complete data exploration.
- Prepare features for modelling.
- Train and evaluate a baseline model.
- Investigate dynamic pressure sensor data.
- Document findings and limitations.

## Dataset

**Dataset source:** [Zenodo — DOI: 10.5281/zenodo.15096167](https://doi.org/10.5281/zenodo.15096167)

**Dataset licence:** Creative Commons Attribution 4.0 International (CC BY 4.0).

The dataset contains hourly records and anomaly scores from an anonymized urban water distribution network. The `fault_d7` label indicates proximity to recorded leak events within a seven-day window; it does not necessarily indicate an active leak at the exact timestamp.

The original dataset is excluded from this repository. Users must obtain it from the source and follow its licence and attribution requirements.

The initial dataset contains 8,737 records and 20 columns, including a timestamp, a target label (`fault_d7`), and sensor-related features.

The `fault_d7` label identifies records within the dataset's defined seven-day window around confirmed leak events. It does not establish that a leak was actively occurring at the exact timestamp.

The original CSV and the Dynamic Pressure Sensor ZIP are stored locally and are excluded from Git commits. Dataset documentation and redistribution terms must be checked before sharing any dataset files.

## Project Structure


AquaGuard/
|-- data/
|-- models/
|-- notebooks/
|   |-- 01_data_exploration.ipynb
|-- reports/
|-- src/
|   |-- main.py
|-- .gitignore
|-- README.md
|-- requirements.txt


## Technology Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Git and GitHub

## Getting Started

Clone the repository and install the required dependencies:

```bash
python -m pip install -r requirements.txt
```

Open the notebook:

`notebooks/01_data_exploration.ipynb`

The dataset is not included in the repository. Place the authorized dataset files in the local `data/` directory before running the notebook.

## Disclaimer

This is an educational machine learning project. Model predictions require appropriate validation and should not be treated as confirmed leak detections or used as the sole basis for operational decisions.