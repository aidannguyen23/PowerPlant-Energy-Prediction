# Combined Cycle Power Plant Regression

This repository contains code and analysis for predicting the net hourly electrical energy output of a Combined Cycle Power Plant using ambient variables (Temperature, Ambient Pressure, Relative Humidity, Exhaust Vacuum) over a span of 6 years (2006-2011) when the plant operated at full load.

## Overview

### The Dataset

The dataset comprises 9568 data points collected during the plant's operation, and various regression techniques were employed to forecast the energy output. 
This project explores the implementation of linear regression and neural network models for prediction and compares their performance.

The dataset comes from the UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/294/combined+cycle+power+plant
Tfekci, Pnar and Kaya, Heysem. (2014). Combined Cycle Power Plant. UCI Machine Learning Repository. https://doi.org/10.24432/C5002N.

### **Additional Variable Information:**
Features consist of hourly average ambient variables 
- Temperature (T) in the range 1.81°C and 37.11°C,
- Ambient Pressure (AP) in the range 992.89-1033.30 milibar,
- Relative Humidity (RH) in the range 25.56% to 100.16%
- Exhaust Vacuum (V) in the range 25.36-81.56 cm Hg
- Net hourly electrical energy output (PE) 420.26-495.76 MW
The averages are taken from various sensors located around the plant that record the ambient variables every second. The variables are given without normalization. 

## Code and Technicalities

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
   - Utilized the Temperature variable to predict energy output.
   - Achieved a correlation coefficient of 0.898.
  
<img src="https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/78a999de-6c9d-4b5d-924f-71e003020cd5" width="50%">

  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/d4d087b5-9048-4236-9336-f01f300cecc3)

  ### 2. Multiple Linear Regression
  - Implemented a neural network model using all of the variables for prediction.
  - Improved the correlation coefficient to 0.926.
    
<img src="https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/7d3beee8-7459-4a74-bac7-d7a81fe1be87" width="50%">

## **Neural Network Regression:**
   - Implemented neural networks for energy output prediction.
   - Explored various architectures and regularization techniques.
   - Visualized model performance and convergence using loss plots.

  ### 1. Standard Regression with Neural Network
  - Explored single-layer and single-node neural network architecture with regression for energy output prediction.
  - Following Standard Linear Regression, I again utilized the Temperature variable to predict energy output.
  - Used regularization techniques for model performance enhancement: (Dropout, L1 regularization, patience, learning rate)
    
  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/b07b8cdf-9477-4611-a2ad-be433b4bb2a1)

  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/fc17d91f-759f-4963-9046-076ed2a32182)


  ### 2. Multiple Regression with Neural Network
  - Implemented a neural network model using all variables for prediction.
  - Following Multiple Linear Regression, I utilized all variables to predict the energy output.
  - Used regularization techniques for model performance enhancement: (Dropout, L1 regularization, patience, learning rate)

  ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/aede1b06-a8fc-402b-b187-86b16a813238)


### Results and Conclusions

#### Mean Squared Error:

<img src="https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/d64486ef-4263-4c8c-b7a3-9e9506573ee5" width="50%">


  - **Multiple Linear Regression** achieved a high correlation coefficient of 0.926, showcasing good predictive capability.
  - The mean squared error (MSE) for neural networks (162.79) was higher compared to linear regression (21.71).
  - As demonstrated by the data trends it is clear that linear regression makes more sense as the data is linear, and thus why linear regression outperforms neural networks.

    ![image](https://github.com/aidannguyen23/PowerPlant-Energy-Prediction/assets/34725584/45010297-f432-4f7e-a969-56f2252c6ad9)

