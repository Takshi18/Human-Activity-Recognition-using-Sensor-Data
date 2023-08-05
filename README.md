# A comparative study of different approaches to HAR using sensor data

## Introduction

This repository presents a comparison of various deep learning models for Human Activity Recognition (HAR) using time series data. Two datasets, UCI-HAR and WISDM, were utilized to evaluate the performance of different models.

## Datasets

### UCI-HAR Dataset
- Dataset Link: [UCI-HAR Dataset](https://archive.ics.uci.edu/dataset/364/smartphone+dataset+for+human+activity+recognition+har+in+ambient+assisted+living+aal)
- Description: The UCI-HAR dataset captures smartphone sensor signals (accelerometer and gyroscope) during daily activities. Data was preprocessed to extract relevant features.
- Features: Various time and frequency domain signals, such as tBodyAcc-XYZ, tGravityAcc-XYZ, fBodyAcc-XYZ, etc.
- Labels: Encoded labels representing activities like WALKING, WALKING_UPSTAIRS, etc.

### WISDM Dataset
- Dataset Link: [WISDM Dataset](https://www.cis.fordham.edu/wisdm/dataset.php)
- Description: The WISDM dataset provides raw sensor data from smartphones. Deep learning models were directly applied to this dataset.
- Labels: Similar to UCI-HAR, activities are encoded as numbers from 1 to 6.

## Models and Files

### UCI-HAR Dataset
1. Machine Learning Models
   - Various machine learning models applied on the pre-engineered UCI-HAR dataset.

2. Deep Learning Models
   - 1-Layered LSTM
   - 2-Layered LSTM
   - CNN-GRU

3. Soft Attention Mechanism
   - Applied on UCI-HAR dataset

### WISDM Dataset
1. Deep Learning Models
   - LSTM
   - CNN-GRU
   - Soft Attention Mechanism

## Data Preprocessing

- Raw sensor data from smartphones was preprocessed:
  - Noise filters were applied.
  - Signals were sampled using fixed-width windows.
  - Separation of body and gravity signals using low-pass filter.
  - Computation of jerk signals, magnitudes, and FFT.
  - Derivation of statistical properties like mean, std, max, etc., and angle-based features.

## Labels

Activities are encoded as follows:
1. WALKING
2. WALKING_UPSTAIRS
3. WALKING_DOWNSTAIRS
4. SITTING
5. STANDING
6. LAYING

## Usage

Clone the repository and navigate to the respective model directories to explore the implementations.

## References

- UCI-HAR Dataset: [Dataset Link](https://archive.ics.uci.edu/dataset/364/smartphone+dataset+for+human+activity+recognition+har+in+ambient+assisted+living+aal)
- WISDM Dataset: [Dataset Link](https://www.cis.fordham.edu/wisdm/dataset.php)

Feel free to contribute or use this code for your own projects!




