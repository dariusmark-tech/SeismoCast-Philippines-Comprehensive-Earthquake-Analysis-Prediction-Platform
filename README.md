# Philippine Earthquake Research (2016–2025): Analysis & Magnitude Prediction

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-green?logo=scikit-learn&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

> A data science project analyzing historical PHIVOLCS earthquake records from 2016 to 2025 — covering geospatial hotspot mapping, temporal trend discovery, and Random Forest-based magnitude prediction.

---

## 📌 Table of Contents

- [Background](#background)
- [Problem Statement](#problem-statement)
- [Project Objectives](#project-objectives)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Model Performance](#model-performance)
- [Future Work](#future-work)
- [Practical Applications](#practical-applications)

---

## 🌏 Background

The Philippines sits along the **Pacific Ring of Fire**, one of the most seismically active regions on Earth. This makes the archipelago highly vulnerable to frequent and potentially devastating earthquakes, threatening lives, infrastructure, and the nation's socio-economic stability.

---

## ❗ Problem Statement

The unpredictable nature of seismic events requires robust analytical frameworks to understand historical patterns and assess regional risks. There is a critical need for:
- Consolidated, clean datasets from PHIVOLCS records
- Advanced models to identify high-risk zones
- Forecasting tools to support disaster preparedness

---

## 🎯 Project Objectives

| # | Objective | Description |
|---|-----------|-------------|
| 1 | **Data Harmonization** | Consolidate and clean PHIVOLCS data (2016–2025) into a unified master dataset |
| 2 | **Geospatial Analysis** | Use interactive maps and density plots to identify seismically active zones |
| 3 | **Temporal Trend Discovery** | Uncover seasonal, monthly, and yearly patterns in seismic frequency and intensity |
| 4 | **Predictive Modeling** | Build and optimize a machine learning model to predict earthquake magnitudes |

---

## 📁 Project Structure

```
phivolcs_datasets/
├── 2016/
├── 2017/
├── 2018/
├── ...
└── 2024/
notebook.ipynb          # Main analysis notebook
README.md
```

---

## ⚙️ Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/dariusmark-tech/your-repo-name.git
cd your-repo-name
pip install pandas numpy scikit-learn plotly geopandas folium requests beautifulsoup4
```

Or inside the notebook:

```python
!pip install pandas numpy scikit-learn plotly geopandas folium requests beautifulsoup4
```

---

## ▶️ Usage

1. Open `notebook.ipynb` in Jupyter or any compatible environment (e.g., DataLab, VS Code).
2. Run all cells sequentially from top to bottom.
3. The notebook will:
   - Set up the directory structure for year-wise datasets
   - Load and preprocess raw earthquake records
   - Generate interactive maps, heatmaps, and temporal visualizations
   - Train and evaluate a Random Forest Regressor for magnitude prediction

---

## 🔬 Methodology

### 1. Environment Setup
Sets up the folder structure for storing year-wise PHIVOLCS data and installs all required libraries.

### 2. Data Loading & Preprocessing
- Loads raw records across multiple years
- Handles encoding inconsistencies and formatting issues
- Engineers features including:
  - **Seismic zone clustering** via K-Means
  - **Rolling historical statistics** (average magnitude, event count)

### 3. Exploratory Data Analysis (EDA)
- Statistical summaries of magnitude, depth, and location
- Interactive Folium maps for geospatial hotspot visualization
- Temporal plots by month, year, and day of week

### 4. Machine Learning Modeling
- **Algorithm**: Random Forest Regressor
- **Optimization**: GridSearchCV with 3-fold cross-validation
- **Tuned Parameters**: `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`
- **Train/Test Split**: 80% / 20%

---

## 📊 Key Findings

- 📉 Most Philippine earthquakes are **low magnitude** (avg. ~2.50)
- 🌊 Depths vary widely (avg. ~29.64 km), indicating diverse seismic mechanisms
- 🗺️ Seismic activity is concentrated along the **Philippine archipelago**, consistent with known fault systems
- 📅 **No strong cyclical patterns** found by month or day of week
- 🔗 **No clear linear correlation** between magnitude and depth

---

## 🤖 Model Performance

| Metric | Value |
|--------|-------|
| R² Score | ~0.35 |
| Mean Absolute Error (MAE) | ~0.42 magnitude units |

> The model provides a solid baseline. Performance is expected to improve with richer geological features and more advanced architectures.

---

## 🔮 Future Work

- **Feature Engineering**: Add proximity to fault lines, GPS displacement data, satellite imagery
- **Advanced Models**: Explore XGBoost, LightGBM, RNNs, or spatio-temporal graph neural networks
- **Multi-Output Prediction**: Predict depth and location alongside magnitude
- **Uncertainty Quantification**: Provide confidence intervals for predictions
- **Dynamic Clustering**: Adapt seismic zone definitions over time
- **Temporal Forecasting**: Model time-series seismic activity rates

---

## 🏗️ Practical Applications

1. **Disaster Preparedness**: Inform seismic hazard assessments, building codes, and land-use planning
2. **Early Warning Indicators**: Identify zones of elevated seismic risk probabilistically
3. **Infrastructure Planning**: Guide engineers in designing resilient structures for specific regions
4. **Public Awareness**: Communicate earthquake risk patterns to the general public

---

## 📜 Data Source

Data sourced from **[PHIVOLCS](https://www.phivolcs.dost.gov.ph/)** (Philippine Institute of Volcanology and Seismology), the official government agency monitoring seismic activity in the Philippines.

---

## 🧑‍💻 Author: Dariusmark-tech

> Feel free to reach out or contribute via pull requests!

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
