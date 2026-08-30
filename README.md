# Courtyard Shape Energy Prediction

This repository contains the code and models for predicting building energy consumption based on various courtyard architectural shapes (L-Shape, U-Shape, and O-Shape). The project evaluates both Machine Learning (ML) and Deep Learning (DL) approaches to understand how spatial layouts impact thermal behavior and energy efficiency.

> **⚠️ Data Privacy Note**
> The dataset used in this project belongs to a scientific research paper published in the *Data in Brief* journal (2025), titled: *"Dataset on energy consumption in buildings within tropical climate based on design aspects of courtyards"*. 
>
> Due to intellectual property and research data privacy constraints, the original dataset files (`.xlsx`) are not included in this public repository. The provided Jupyter notebooks contain the methodology, AI model architectures (Machine Learning & Deep Learning), and evaluation metrics for reproducibility and demonstration purposes only.

## Project Overview

The goal of this research is to analyze how open, semi-open, and closed courtyard designs influence energy consumption. By applying predictive modeling, we can identify which architectural shapes yield the most predictable and efficient energy profiles.

## Methodology

**Data Preprocessing**
* **Split:** Data was divided into 80% for training and 20% for testing.
* **Scaling:** `StandardScaler` was applied to normalize the features for optimal neural network performance.
* **Augmentation:** `SMOTE` (Synthetic Minority Over-sampling Technique) was utilized to balance the classes and prevent model bias.

**Machine Learning (ML)**
* Evaluated models: **XGBoost** and **Random Forest**.
* XGBoost demonstrated superior capability in handling tabular data and extracting non-linear relationships.

**Deep Learning (DL)**
* Evaluated networks: Artificial Neural Networks (**ANN**), Recurrent Neural Networks (**RNN**), and 1D Convolutional Neural Networks (**1D-CNN**).

## Key Results

| Model | Shape | Accuracy | Notes |
| :--- | :--- | :--- | :--- |
| **XGBoost** | L-Shape (Open) | 95.45% | Exceptional performance and feature extraction. |
| **XGBoost** | U-Shape (Semi-Open)| 94.48% | High accuracy on tabular data. |
| **1D-CNN** | U-Shape (Semi-Open)| 89.61% | Highest performing DL model for this shape. |
| **DL Models** | L-Shape (Open) | ~86.00% | Stable performance across architectures. |
| **All Models**| O-Shape (Closed) | < 47.00% | Sharp decline in predictive accuracy. |

**Scientific Conclusion**
The significant drop in prediction accuracy for the O-Shape (closed courtyard) is attributed to high aerodynamic and thermal complexity. Factors like shadow overlap and heat retention make energy behavior in fully enclosed spaces highly volatile and difficult to predict compared to open (L-Shape) and semi-open (U-Shape) layouts.

## Usage

To run these models, you can execute the provided Jupyter Notebooks via Google Colab.

1. Clone this repository:
   ```bash
   git clone [https://github.com/doaaz1/energy-consumption-in-buildings)
