---
title: "BESTox"
image: 
  path: "" #/assets/img/bestox_logo.jpg        #大图
  thumbnail: /assets/img/bestox_logo.jpg       #小图
  caption: "Photo from [Pexels](https://www.pexels.com)"
---

### A Convolutional Neural Network Regression Model Based on Binary-Encoded SMILES for Acute Oral Toxicity Prediction of Chemical Compounds.

#### :warning: First thing First, the online prediction server is now available at: [BESTox on CBBio](https://cbbio.online/BESTox/)

```python
data_path = '<Replace this string with the path of prediction result file (dnn_output.npy)>'
outout_path = '<Replace this string with the path of output transformed file path + / + output transformed file name>'
# e.g.
data_path = './automatic-ecg-diagnosis-master/dnn_output.npy'
outout_path = './automatic-ecg-diagnosis-master/dnn_output_bin.csv'
```

### 1. What's BESTox
BESTox is a novel convolutional neural network regression model, to predict the acute oral toxicity (LD50) of chemical compounds. In a benchmark experiment using a dataset (Oral Rat LD50 set) of 7413 observations (train/test, 5931/1482), BESTox achieved a squared Pearson correlation coefficient (R2) of 0.619, root-mean-squared error (RMSE) of 0.603, and mean absolute error (MAE) of 0.433.

### 2. Features
This model learns the compositional and chemical properties of compounds from their two-dimensional binary matrices. Each matrix encodes the occurrences of certain atom types, number of bonded hydrogens, atom charge, valence, ring, degree, aromaticity, chirality, and hybridization along the SMILES string of a given compound. This model supports SMILES with max length 300 characters, SMILES with less characters will be padded with 0.

### 3. Architecture
The architecture of our optimized CNN model is presented in Figure. 3. The model contains two convolutional layers (Conv) with 512 and 1024 filters respectively. After each convolutional layer is an average pooling layer and a batch normalization layer (BN). Then, a max pooling layer is used before the learned features fed into the fully connected layers (FC). Four FCs containing 2048, 1024, 512, and 256 hidden nodes were found to be the optimal combination for toxicity prediction and the ReLU function is used to generate the prediction output (-log10(LD50 mol/kg)).
