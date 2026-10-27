<div align="center">

# Automobile Price Regression

**From linear regression to a neural network on the UCI Automobile dataset**

<a href="https://colab.research.google.com/github/Steven-Macas/Automobile-Red-Neuronal/blob/main/red_neuronal_PIA_automobile.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab" /></a> <img src="https://img.shields.io/badge/Python-3-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python: 3" /> <img src="https://img.shields.io/badge/Pandas-data-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas: data" /> <img src="https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn: ML" /> <img src="https://img.shields.io/badge/TensorFlow-Keras-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" alt="TensorFlow: Keras" /> <img src="https://img.shields.io/badge/Seaborn-charts-4C72B0?style=flat-square" alt="Seaborn: charts" />

</div>

## Overview

Price prediction for cars from their technical characteristics, comparing a **linear regression**
baseline with a **Keras neural network**.

## Dataset

[UCI Automobile](https://archive.ics.uci.edu/ml/datasets/automobile) – 205 cars and 26 attributes
(make, fuel type, body style, engine size, horsepower, fuel consumption, insurance risk rating…) plus the price.

## Approach

1. **Missing values** – detection with `isnull()` and correction of the affected columns.
2. **Distributions** – histograms and box plots; transformations to reduce skewness and extreme outliers, then `StandardScaler`.
3. **Feature analysis** – correlation heatmap for numeric features and box plots of price by category.
4. **Split** – training, validation and test sets (about 54 / 26 / 20 %).
5. **Encoding** – one-hot encoding with `DictVectorizer`.
6. **Baseline** – `LinearRegression`.
7. **Neural network** – Dense(64, ReLU) → Dense(32, ReLU) → Dense(1), Adam, MSE loss, 50 epochs.

## Results

<table>
  <tr><td align="center" valign="top"><img src="images/correlation.png" alt="Correlation heatmap" width="280" /><br /><sub>Correlation heatmap</sub></td><td align="center" valign="top"><img src="images/real-vs-predicted.png" alt="Real vs predicted price (test set)" width="280" /><br /><sub>Real vs predicted price (test set)</sub></td><td align="center" valign="top"><img src="images/training-loss.png" alt="Neural network training loss" width="280" /><br /><sub>Neural network training loss</sub></td></tr>
</table>

## How to run

Open the notebook in Colab with the badge above; it downloads the dataset from the UCI repository.

*The notebook is written in Spanish.*

---

<sub>Made by <b>Steven Macas</b> — Data Engineer &amp; Data Analyst · <a href="https://gointy.com">gointy.com</a> · <a href="https://www.linkedin.com/in/steven-macas">LinkedIn</a> · <a href="https://github.com/Steven-Macas">GitHub</a></sub>
