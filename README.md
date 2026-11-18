# Spatiotemporal_Congestion_Anomaly_Detection
# Spatiotemporal Congestion and Anomaly Detection Using Big Data Analytics and Deep Learning on UK Traffic Count Data

## Overview

This repository presents an end-to-end big data analytics and deep learning pipeline designed to detect traffic congestion and anomalous traffic patterns across the United Kingdom road network. By leveraging distributed data processing with **Apache Spark (PySpark)** and temporal-spatial sequence modeling with **Deep Learning**, the project analyzes large-scale hourly traffic count records to classify road conditions, uncover peak congestion bottlenecks, and identify unexpected traffic anomalies.

---

## Key Objectives

* **Distributed Data Engineering:** Ingest, clean, and preprocess large-scale UK Department for Transport (DfT) traffic count datasets using PySpark.
* **Spatiotemporal Exploratory Data Analysis (EDA):** Analyze multi-year traffic volume distributions across road classifications (Motorways, A-roads, Minor roads), regions, and temporal cycles (hourly, daily, seasonal).
* **Anomaly & Congestion Labeling:** Apply statistical outlier detection—including Interquartile Range (IQR) thresholding—to distinguish normal traffic flow from severe congestion and anomalous events.
* **Deep Learning Modeling:** Train and evaluate neural network architectures to classify traffic states and predict congestion patterns based on spatiotemporal and contextual features.

---

## Dataset

* **Source:** UK Department for Transport (DfT) Road Traffic Statistics (Hourly Traffic Count Data)
* **Key Features:**
  * **Spatial Attributes:** Region, Local Authority, Road Name, Road Category, Count Point ID, Latitude/Longitude
  * **Temporal Attributes:** Year, Count Date, Hour of Day, Day of Week
  * **Traffic Metrics:** Vehicle counts broken down by vehicle type (pedal cycles, two-wheeled motor vehicles, cars and taxis, buses and coaches, LGVs, HGVs) and total motor vehicle volume

---

## Methodology & Pipeline

1. **Data Ingestion & Preprocessing (PySpark)**
   * Schema enforcement, missing value imputation, and duplicate removal across multi-million-row CSV datasets.
   * Feature engineering for cyclical temporal variables, road-type encodings, and aggregated vehicle flow ratios.
2. **Statistical Anomaly Detection**
   * Calculation of road-specific baseline distributions and IQR thresholds to flag abnormal surges or drops in vehicle counts.
3. **Deep Learning Classification & Forecasting**
   * Normalization and sequence/tabular tensor preparation.
   * Model training using deep neural architectures (MLP / LSTM / 1D-CNN) with class-imbalance handling and validation tracking.
4. **Evaluation**
   * Assessed using Accuracy, Precision, Recall, F1-Score, and Confusion Matrix analysis across normal and congested/anomalous classes.

---

## Repository Structure

```text
Spatiotemporal_Congestion_Anomaly_Detection/
├── Spatiotemporal_Congestion_Anomaly_Detection.ipynb   # Main PySpark & Deep Learning notebook
└── README.md                                           # Project documentation
