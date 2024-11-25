# Predictive Maintenance with Neural Networks and SOMs 🚀

## 📖 Overview
This project focuses on applying machine learning techniques, including **neural networks** and **Self Organizing Maps (SOMs)**, to **Predictive Maintenance**. The goal is to predict tool wear and failure types in a manufacturing environment based on sensor data. By leveraging **anomaly detection**, **predictive modeling**, and **dimensionality reduction**, we aim to improve maintenance scheduling and avoid costly downtimes.

The dataset comes from [Kaggle](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification) and was created by Shivam Bansa. It’s a synthetic dataset designed to mimic real-world industrial predictive maintenance data. The measurements simulate a production system where parts are manufactured using a central tool. Once a part is completed, it’s removed, and the next part is set up. The tool experiences wear during production, which can lead to a "Tool wear" failure. After such a failure, the tool is replaced, and production continues. Alongside tool wear failures, other issues like power or overload failures are also included in the dataset.

The main goal of this analysis is to minimize downtime in the (fictional) production system. To achieve this, predictive maintenance techniques are applied, alongside anomaly detection to prevent machine behavior that could lead to failures.

## 📚 Table of Contents
1. **Business Understanding**
2. **Data Understanding**
3. **Data Preparation**
    1. Data cleaning
    2. Data normalization
    3. Data transformation
    4. Missing value treatment
    5. Imbalanced data treatment
    6. Feature engineering
4. **Modeling**
    1. Training a neural network for anomaly detection
    2. Training a decision tree for anomaly detection
    3. Predictive Maintenance
5. **Evaluation**

## ⚙️ Key Techniques
- **Data Preprocessing**: Standardization and feature engineering are applied to ensure the models receive clean and well-processed data.
- **Neural Networks (NN)**: Used for anomaly detection and failure type prediction. The output is a probability of failure for each dataset, which helps detect potential issues early on.
- **Self Organizing Maps (SOM)**: A type of neural network that reduces dimensionality and visualizes high-dimensional data in a 2D map. Used for clustering and analyzing failure patterns.
- **Similarity Model for RUL Prediction**: The Remaining Useful Life (RUL) is predicted using historical data and the similarity between current and past time series.

## 🛠️ Features
- **Anomaly Detection**: Identifies patterns and anomalies in sensor data.
- **Failure Type Prediction**: Predicts different types of failures (e.g., Power, Overstrain, Random Failure).
- **Condition Indicator**: Utilizes failure probability trends as a condition indicator to forecast when maintenance should occur.
- **RUL Prediction**: Estimates the Remaining Useful Life of tools based on historical data using a similarity model.
- **SOM Visualization**: Provides a 2D visualization of high-dimensional sensor data and failure types, helping to identify clusters and patterns.

## 💡 TL;DR
The neural network successfully predicts failure types but struggles with distinguishing "No Failure" from actual failures.
The SOM clusters data and visualizes failure patterns, but Random Failures appear to be scattered randomly across the map.
Using SMOTE for balancing the dataset did not yield significant improvements.
The RUL prediction shows promising results, though further optimization is needed for consistently accurate predictions.