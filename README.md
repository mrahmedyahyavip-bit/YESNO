# YESNO Audio Classification Mini-Project

## Overview

This project implements binary speech classification using the TorchAudio YESNO dataset.

The objective is to classify individual spoken words as Yes or No using MFCC acoustic features and four machine learning classifiers.

## Dataset

- Dataset: TorchAudio YESNO
- Total recordings: 60
- Words per recording: 8
- Total speech samples: 480
- Sampling rate: 8,000 Hz
- Classes: No (0), Yes (1)

## Methodology

1. Load and explore the audio dataset.
2. Visualize waveforms and extract MFCC features.
3. Perform energy-based speech segmentation.
4. Optimize segmentation parameters and verify speech intervals.
5. Extract 26 MFCC-based features per word.
6. Split the dataset by original recording into training and testing subsets.
7. Train four machine learning classifiers.
8. Evaluate and compare their performance.
9. Perform five-fold group-based cross-validation.

## Classification Models

- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Random Forest
- Multi-Layer Perceptron (MLP)

## Results

| Classifier | Test Accuracy | Mean CV Accuracy |
|---|---:|---:|
| SVM | 100% | 99.38% |
| KNN | 100% | 99.38% |
| Random Forest | 100% | 99.38% |
| MLP | 100% | 99.38% |

The test set contained 96 word-level samples, and the five-fold cross-validation used recording-level groups.

## Technologies

Python, PyTorch, TorchAudio, Librosa, NumPy, Pandas, Matplotlib, and Scikit-learn.

## Limitations

The experiments were conducted on a small dataset. Segmentation parameters were adjusted after inspecting recordings, and performance on independent datasets has not been established.

## Conclusion

The experiment demonstrates that MFCC-based features can support highly accurate Yes/No classification on the evaluated YESNO dataset. Additional testing is recommended to assess generalization under more diverse recording conditions.
