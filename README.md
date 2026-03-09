# EEG-Based Emotion Recognition using Deep Learning

> **Collaboration Note**: This project was developed as a partnered research effort with **ajrajn**.

## Project Overview
This repository implements advanced deep learning workflows for classifying emotional states from EEG signals using the **SEED (SJTU Emotion EEG Dataset)**. The study compares two distinct methodologies for brain-state decoding:
1.  **Pure Deep Learning**: Direct classification using raw EEG signal inputs.
2.  **Hybrid Deep Learning**: Feature-driven classification utilizing **Spectrogram** representations of neural activity.

## Dataset
* **Source**: SEED Dataset.
* **Content**: High-density EEG recordings from subjects viewing emotional film clips.
* **Labels**: Positive, Neutral, and Negative emotional states.

## Methodology
The pipeline involves rigorous signal processing and model training:

* **Pre-processing**: Data cleaning, segmentation, and normalization of multi-channel EEG signals.
* **Feature Extraction (Hybrid Path)**: Generation of time-frequency spectrograms to capture non-stationary neural dynamics.
* **Model Architecture**: Implementation of **EEGNet**, a compact convolutional neural network designed specifically for BCI tasks, leveraging depthwise and separable convolutions.
* **Evaluation Strategy**: Employed a **Leave-One-Subject-Out (LOSO)** cross-validation approach to ensure model generalizability across different individuals.

## Results
The performance was benchmarked using the F1-score to account for class distribution:
* **Mean F1-Score**: 0.707.
* **Peak Performance**: Individual subject classification reached F1-scores as high as **0.923**.

## Implementation Details
* **Framework**: TensorFlow/Keras
* **Signal Processing**: Scipy, NumPy
* **Visualization**: Matplotlib
