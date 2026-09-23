# 🌱 Regional Carbon Emission Mapping in Yogyakarta

A geospatial machine learning study for **mapping and predicting areas with high carbon emission potential in the Special Region of Yogyakarta (DIY), Indonesia**, using spatial data extracted from **OpenStreetMap through OSMnx**.

The study compares the performance of **Random Forest** and **XGBoost** classification algorithms to identify areas with different levels of carbon emission potential based on spatial characteristics.

---

## 📌 Project Overview

Carbon emissions are closely related to spatial characteristics such as transportation networks, built-up areas, land use, and urban activity.

This project explores the use of **geospatial data and machine learning** to identify areas with high carbon emission potential in the Special Region of Yogyakarta.

Spatial data obtained using **OSMnx** is processed into machine learning features and used to train two classification models:

* **Random Forest**
* **XGBoost**

The models are evaluated using several classification metrics to compare their predictive performance in a geospatial context.

---

## 🎯 Objectives

The main objectives of this study are:

* Map spatial characteristics related to carbon emission potential.
* Process OpenStreetMap-based spatial data using OSMnx.
* Develop machine learning models for carbon emission potential classification.
* Compare Random Forest and XGBoost performance.
* Evaluate models using accuracy, precision, recall, and F1-score.
* Analyze model predictions using confusion matrices.
* Visualize predicted high-emission-potential areas spatially.

---

## 🗺️ Study Area

**Special Region of Yogyakarta (Daerah Istimewa Yogyakarta / DIY), Indonesia**

The analysis is limited to spatial data within the DIY administrative region.

---

## 🔬 Methodology

The overall methodology consists of several stages.

### 1. Spatial Data Collection

Spatial data is collected from **OpenStreetMap** using the OSMnx library.

Potential spatial features include:

* Road networks
* Road density
* Building distribution
* Points of interest
* Land-use characteristics
* Transportation-related features

The extracted spatial information is transformed into numerical features suitable for machine learning.

---

### 2. Data Preprocessing

The spatial dataset is prepared through:

* Data cleaning
* Geometry validation
* Coordinate system transformation
* Feature extraction
* Missing-value handling
* Feature normalization where required
* Target-label preparation

The processed spatial data is then converted into a machine-learning-ready dataset.

---

### 3. Feature Engineering

Spatial features are generated from the OSM-based data to represent characteristics that may be associated with carbon emission potential.

Examples include:

```text
Road Density
Building Density
Road Length
POI Density
Intersection Density
Land-use Characteristics
```

These features are used as independent variables for the classification models.

---

### 4. Machine Learning Models

Two supervised machine learning algorithms are compared.

#### Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees to produce a classification result.

Its advantages for this type of analysis include:

* Ability to model nonlinear relationships
* Robustness to noisy features
* Ability to capture feature interactions
* Relatively low preprocessing requirements

#### XGBoost

XGBoost is a gradient boosting algorithm that sequentially builds decision trees to minimize prediction errors.

It is used as a second model to provide a performance comparison against Random Forest.

---

## 📊 Model Evaluation

The models are evaluated using several classification metrics.

### Accuracy

Measures the proportion of correctly classified observations.

```text
Accuracy = Correct Predictions / Total Predictions
```

### Precision

Measures the proportion of predicted positive observations that are actually positive.

```text
Precision = TP / (TP + FP)
```

### Recall

Measures the proportion of actual positive observations correctly identified by the model.

```text
Recall = TP / (TP + FN)
```

### F1-Score

Provides a harmonic mean between precision and recall.

```text
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

### Confusion Matrix

The confusion matrix is used to examine the distribution of:

* True Positive
* True Negative
* False Positive
* False Negative

---

## 🔄 Analysis Workflow

```text
OpenStreetMap
      │
      ▼
     OSMnx
      │
      ▼
Spatial Data Extraction
      │
      ▼
Data Cleaning & Preprocessing
      │
      ▼
Spatial Feature Engineering
      │
      ▼
Feature Dataset
      │
      ├───────────────┐
      ▼               ▼
Random Forest      XGBoost
      │               │
      └───────┬───────┘
              ▼
       Model Evaluation
              │
              ▼
 Accuracy • Precision
 Recall • F1-Score
 Confusion Matrix
              │
              ▼
     Spatial Prediction
              │
              ▼
Carbon Emission Potential Map
```

---

## 🧠 Model Comparison

The study compares Random Forest and XGBoost using the same dataset and evaluation framework.

| Metric    | Random Forest | XGBoost |
| --------- | ------------: | ------: |
| Accuracy  |             — |       — |
| Precision |             — |       — |
| Recall    |             — |       — |
| F1-Score  |             — |       — |

> The table can be populated with the final experimental results.

Rather than relying on a single metric, the comparison considers multiple evaluation measures to provide a broader view of model performance.

---

## 🗺️ Spatial Prediction

After model training, the selected spatial features are passed through the trained classifiers to generate predictions for geographic areas within DIY.

The resulting predictions can be visualized as a spatial map showing areas classified according to their carbon emission potential.

Example conceptual output:

```text
┌───────────────────────────────────┐
│       YOGYAKARTA REGION           │
│                                   │
│   Low Potential     Medium        │
│        ███            ███         │
│                                   │
│                 High Potential    │
│                     █████         │
│                                   │
│        Spatial Prediction Map     │
└───────────────────────────────────┘
```

---

## 🛠️ Technologies

* **Python**
* **OSMnx** — OpenStreetMap spatial data extraction
* **GeoPandas** — Geospatial data processing
* **Pandas** — Data manipulation
* **NumPy** — Numerical computation
* **Scikit-learn** — Machine learning and evaluation
* **XGBoost** — Gradient boosting classification
* **Matplotlib** — Visualization
* **Seaborn** — Statistical visualization
* **Jupyter Notebook** — Experimentation and analysis

---

## 📁 Project Structure

```text
yogyakarta-carbon-emission-mapping/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── carbon_emission_analysis.ipynb
│
├── src/
│   ├── data_collection.py
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── random_forest.py
│   ├── xgboost_model.py
│   └── visualization.py
│
├── outputs/
│   ├── maps/
│   ├── metrics/
│   └── figures/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 📈 Expected Outputs

The project produces several analytical outputs:

### 1. Spatial Distribution Map

Visualization of OSM-based spatial features across DIY.

### 2. Feature Dataset

Processed spatial features used as input for machine learning.

### 3. Model Performance

Evaluation results for:

* Accuracy
* Precision
* Recall
* F1-score

### 4. Confusion Matrix

Visualization of classification errors and correctly classified observations.

### 5. Carbon Emission Potential Map

Spatial visualization of model predictions across the study area.

---

## ⚠️ Scope & Limitations

This study focuses specifically on the relationship between **geospatial characteristics and carbon emission potential**.

The analysis is limited to spatial data from the Special Region of Yogyakarta and does not incorporate several external factors, including:

* Weather conditions
* Socioeconomic variables
* Energy consumption
* Population behavior
* Industrial emission measurements
* Government policies
* Temporal changes in emissions

Therefore, the resulting predictions should be interpreted within the context of the available geospatial features rather than as direct measurements of actual carbon emissions.

---

## 🚀 Future Development

Several improvements can be explored in future research:

* Integrating official carbon emission datasets.
* Incorporating population density and socioeconomic variables.
* Adding weather and climate data.
* Including temporal datasets for time-series analysis.
* Using satellite imagery for land-use analysis.
* Comparing additional machine learning algorithms.
* Applying hyperparameter optimization.
* Using SHAP for model interpretability.
* Developing an interactive GIS dashboard.
* Integrating real-time or periodically updated OSM data.

---

## 📚 Research Context

This project demonstrates the integration of **Geographic Information Systems (GIS), OpenStreetMap data, spatial feature engineering, and machine learning** for environmental analysis.

The comparison between Random Forest and XGBoost provides an empirical framework for evaluating how different tree-based ensemble methods perform when applied to geospatial classification problems.

---

## 👨‍💻 Author

**Naufal El Kamil**

Data Science & Machine Learning Enthusiast
Indonesia

---

## 📄 License

This project is intended for **educational, research, and portfolio purposes**.
