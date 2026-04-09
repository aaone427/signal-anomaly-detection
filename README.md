# Signal Anomaly Detection — Time-Series Classification Pipeline

## Overview
A machine learning pipeline for classifying anomalous patterns in variable-length time-series signals. 
Originally applied to ECG biosensor data, the methods — including feature extraction, PCA-based dimensionality reduction, and Decision Tree/Random Forest classification
 — are directly transferable to industrial fault detection in vibration, pressure, and current sensor streams.

## Industrial Applicability
| This Project | Industrial Equivalent |
|---|---|
| ECG amplitude sequence | Vibration/current sensor reading |
| Abnormal heartbeat | Bearing fault, motor anomaly |
| PCA feature compression | Dimensionality reduction for high-freq sensor data |
| Random Forest classifier | Ensemble fault detector |
| 10-fold CV + Wilcoxon test | Statistically validated model comparison |

## Pipeline Summary
This project originally uses an ECG dataset to classify normal and abnormal heartbeats, 
then expanded for classifying anomalous patterns in variable-length time-series signals with
2,596 labeled instances remaining after data cleaning. Feature engineering was
performed to construct an analytical base table (ABT), followed by Principal
Component Analysis (PCA), where the first three principal components retained
83.7% of the variance and reduced multicollinearity. The data was then partition into training and testing set.
Decision Tree and Random Forest classifiers were trained and optimised using GridSearch with cross-
validation to improve generalisation. Both models achieved high performance with
F1 scores of approximately 0.97; while the Decision Tree slightly outperformed
the Random Forest on a single split, 10-fold cross-validation and a Wilcoxon test
(p = 0.25) showed no statistically significant difference 

## Key Results
- Dataset: 2,596 labeled instances after cleaning
- Features: 5 engineered statistical features → reduced to 3 PCA components (83.7% variance retained)
- Decision Tree F1: 0.973
- Random Forest F1: 0.971
- 10-fold CV average F1: 0.97 (both models, difference not statistically significant)

## Tools
Python, scikit-learn, pandas, numpy, matplotlib, seaborn

## Author


