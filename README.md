# Physiological Stress Detection Using Deep Learning

A multimodal deep learning system for **subject-independent physiological stress detection** using the **WESAD (Wearable Stress and Affect Detection)** dataset.

## Overview

This graduation project focuses on detecting physiological stress from wearable sensor data using deep learning. The system uses physiological signals collected from both **chest and wrist sensors**, along with **Heart Rate Variability (HRV)** features.

The main approach combines predictions from different physiological modalities through **decision-level majority-vote fusion**. Multiple deep learning architectures were also implemented and compared, with evaluation performed using **Leave-One-Subject-Out (LOSO) cross-validation** to test how well the models generalize to unseen subjects.

## Models

The project explored multiple deep learning approaches, including:

* **CNN-LSTM** for learning spatial and temporal patterns from physiological signals.
* **CNN-Transformer** for combining convolutional feature extraction with Transformer-based temporal modelling.
* Additional temporal and spectrogram-based architectures for comparative evaluation.

## Dataset

The project uses the **WESAD dataset**, which contains physiological and motion data collected during different affective and stress-inducing conditions.

The signals used in the project include:

* ECG
* EDA
* EMG
* Respiration
* Temperature
* BVP
* Accelerometer (ACC)
* HRV features

Data from both **chest** and **wrist** sensor platforms were processed and used for model development.

## Methodology

The overall pipeline consists of data loading, preprocessing, signal segmentation, feature engineering, model training, and evaluation.

Physiological signals were processed into fixed-length time windows, while HRV features were extracted for use as an additional modality. Separate models were trained for different physiological modalities, and their predictions were combined using decision-level majority voting.

To evaluate subject-independent performance, **Leave-One-Subject-Out (LOSO) cross-validation** was used. In each fold, data from one subject was held out for testing while the remaining subjects were used for training.

## Results

The multimodal decision-level fusion approach achieved:

| Metric   |     Score |
| -------- | --------: |
| Accuracy | **95.0%** |
| F1-Score | **0.916** |

Performance was evaluated using accuracy, precision, recall, and F1-score.

## Technologies

**Programming Language:** Python

**Deep Learning:** PyTorch

**Machine Learning:** Scikit-learn

**Data Processing:** Pandas, NumPy

**Development Environment:** Jupyter Notebook

## Project Structure

```text
Physiological-Stress-Detection/
│
├── data/
│   └── WESAD/
│
├── notebooks/
│   ├── NB1_Data_Acquisition.ipynb
│   ├── NB2_Preprocessing.ipynb
│   ├── NB3_Model_Training_Evaluation.ipynb
│   └── NB4_Analysis_Plots.ipynb
│
├── models/
│
├── results/
│
├── README.md
└── requirements.txt
```

## Evaluation

The models were evaluated using **Leave-One-Subject-Out Cross-Validation (LOSO-CV)** to provide a more realistic assessment of generalization to subjects not seen during training.

The evaluation focused on:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrices
* Modality contribution
* Comparison of temporal and spectral representations

## Project Goal

The goal of this project was not only to achieve high classification performance, but also to investigate how different physiological modalities and deep learning architectures contribute to **subject-independent stress detection**.

## Academic Project

**Graduation Project — University of Hertfordshire**

**Title:** Physiological Stress Detection Using Deep Learning
