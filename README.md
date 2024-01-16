# Cheminformatics Project #1 - Solubility Prediction Model

## Overview

This repository hosts a linear regression model for predicting aqueous solubility (LogS) using molecular descriptors. It follows the methodologies by Delaney and Pat Walters, aiming to refine the prediction of solubility from chemical structures.

## Features

- Implements linear regression with descriptors: LogP, Molecular Weight, Rotating Bonds, Aromatic Proportion.
- Data consists of 1143 molecules taken from the 2004 paper by Delaney on predicting solubility, ref below, and splits the data 80:20, training:testing
- Evaluation of model performance using MSE and R^2.
- Visualization of model predictions against experimental data.

## Contents

- `solubility_model.py`: Main Python script for model training and evaluation.
- `data/`: Dataset directory.
- `notebooks/`: Jupyter notebooks for exploratory data analysis.
- `requirements.txt`: Required Python libraries.
- `plots/`: Visualizations of model performance.

## Key Takeaways
The left subplot compares actual vs. predicted LogS for training data, and the right subplot does the same for test data, both showing linear regression lines to assess model fit and generalization.

The model shows a good fit for the training data with a tighter clustering around the best-fit line, indicating accurate predictions within the scope of the data it was trained on.

Nonetheless, the test data does show more spread around the best-fit line / looser clustering, suggesting the model's predictions are less precise when encountering new data.

The observed variation may come from the model overfitting to the training data or the inherent diversity and complexity within the test dataset that wasn't captured during training.

Enhancements to the model could include cross-validation to ensure it generalizes well, regularisation to prevent overfitting, and possibly expanding the training data to encompass a broader variety of data points.

Exploring feature engineering to better capture the underlying data patterns or tweaking hyperparameters could also contribute to a more robust model performance.

![scaterr](https://github.com/lankan01/cheminfor_projects/assets/108777684/72e9bc87-23b9-4788-8ae2-7682e351524f)


## Getting Started

### Prerequisites

List any software, libraries, or dependencies that users need to have installed or set up before they can run your Google Colab notebook. For example:

- [Google Colab](https://colab.research.google.com/): This notebook is designed to be run in Google Colab. You can open it directly in Colab by clicking the "Open in Colab" badge at the top of the notebook.

### Usage

Explain how to use your notebook, including any important steps or configurations. You can include details like:

1. Click the "Open in Colab" badge to open the notebook in Google Colab.
2. Follow the instructions within the notebook to execute code cells and obtain results.
3. Provide any additional information or context that might be helpful for users when running your notebook.


## References
- John S. Delaney. ESOL:  Estimating Aqueous Solubility Directly from Molecular Structure. J. Chem. Inf. Comput. Sci. 2004, 44, 3, 1000-1005.

- Pat Walters. Predicting Aqueous Solubility - It's Harder Than It Looks. Practical Cheminformatics Blog

- Bharath Ramsundar, Peter Eastman, Patrick Walters, and Vijay Pande. Deep Learning for the Life Sciences: Applying Deep Learning to Genomics, Microscopy, Drug Discovery, and More, O'Reilly, 2019.

- Chanin Nantasenamat - The Data Professor, Cheminformatics in Python
  
- Supplementary file from Delaney's ESOL:  Estimating Aqueous Solubility Directly from Molecular Structure.

