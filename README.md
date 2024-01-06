# Combined Cycle Power Plant Regression

This repository contains code and analysis for predicting the net hourly electrical energy output (EP) of a Combined Cycle Power Plant using ambient variables (Temperature, Ambient Pressure, Relative Humidity, Exhaust Vacuum) over a span of 6 years (2006-2011) when the plant operated at full load.

## Overview

The dataset comes from the UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/294/combined+cycle+power+plant
Tfekci, Pnar and Kaya,Heysem. (2014). Combined Cycle Power Plant. UCI Machine Learning Repository. https://doi.org/10.24432/C5002N.

The dataset comprises 9568 data points collected during the plant's operation, and various regression techniques were employed to forecast the energy output. This project explores the implementation of linear regression and neural network models for prediction and compares their performance.

## Code and Analysis

### Tools and Libraries Used

- Python
- Pandas, NumPy, Matplotlib
- TensorFlow, Scikit-learn

### Files

- `Folds5x2_pp.xlsx` renamed to `Power_Plant_Energy_Production.xlsx` for purposes of this repository: Dataset file containing power plant variables and energy output.
- `CCPP_Regression.ipynb`: Jupyter Notebook containing code for data preprocessing, model implementation (linear regression and neural network), visualization, and evaluation.

# Methods Explored

## **Linear Regression:**
   - Utilized ambient variables independently to predict energy output.
   - Evaluated performance and correlation coefficients.

  ### 1. Standard Linear Regression
   - Had a correlation coefficient of 0.898:

<img src="https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/78a999de-6c9d-4b5d-924f-71e003020cd5" width="50%">

  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/d4d087b5-9048-4236-9336-f01f300cecc3)

  ### 2. Multiple Linear Regression
  - Had a better correlation coefficient of 0.926:
    
<img src="https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/7d3beee8-7459-4a74-bac7-d7a81fe1be87" width="50%">

## **Neural Network Regression:**
   - Implemented neural networks for energy output prediction.
   - Explored various architectures and regularization techniques.
   - Visualized model performance and convergence using loss plots.

  ### 1. Standard Regression with Neural Network
  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/b07b8cdf-9477-4611-a2ad-be433b4bb2a1)

  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/fc17d91f-759f-4963-9046-076ed2a32182)


  ### 2. Multiple Regression with Neural Network
  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/aede1b06-a8fc-402b-b187-86b16a813238)


### Results and Conclusions

#### Mean Squared Error:

<img src="https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/d64486ef-4263-4c8c-b7a3-9e9506573ee5" width="50%">


- **Linear Regression:**
  - Achieved a high correlation coefficient of 0.926, showcasing good predictive capability.

- **Neural Network Regression:**
  - The mean squared error (MSE) for neural networks was higher compared to linear regression.
