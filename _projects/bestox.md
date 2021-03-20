---
title: "BESTox"
image: 
  path: /assets/img/bestox_logo.png        #大图
  thumbnail: /assets/img/bestox_logo_sm.png       #小图
  caption: ""
---

### A Convolutional Neural Network Regression Model Based on Binary-Encoded SMILES for Acute Oral Toxicity Prediction of Chemical Compounds.

##### :fire: Online prediction server is available at: [BESTox on CBBio](https://cbbio.online/BESTox/) :fire:
##### :beginner: More details could be found at: [Here](https://cbbio.online/BESTox/?action=datamethod)

### 1. What's BESTox ?
BESTox is a novel convolutional neural network regression model, to predict the acute oral toxicity (LD50) of chemical compounds. In a benchmark experiment using a dataset (Oral Rat LD50 set) of 7413 observations (train/test, 5931/1482), BESTox achieved a squared Pearson correlation coefficient (R2) of 0.619, root-mean-squared error (RMSE) of 0.603, and mean absolute error (MAE) of 0.433.

### 2. Features
This model learns the compositional and chemical properties of compounds from their two-dimensional binary matrices. Each matrix encodes the occurrences of certain atom types, number of bonded hydrogens, atom charge, valence, ring, degree, aromaticity, chirality, and hybridization along the SMILES string of a given compound. This model supports SMILES with max length 300 characters, SMILES with less characters will be padded with 0.

### 3. Architecture
The architecture of our optimized CNN model is presented in Figure. 3. The model contains two convolutional layers (Conv) with 512 and 1024 filters respectively. After each convolutional layer is an average pooling layer and a batch normalization layer (BN). Then, a max pooling layer is used before the learned features fed into the fully connected layers (FC). Four FCs containing 2048, 1024, 512, and 256 hidden nodes were found to be the optimal combination for toxicity prediction and the ReLU function is used to generate the prediction output (-log10(LD50 mol/kg)).

If this server helped you, please cite the following paper:
```
@inproceedings{chen2020bestox,
  title={Bestox: A convolutional neural network regression model based on binary-encoded SMILES for acute oral toxicity prediction of chemical compounds},
  author={Chen, Jiarui and Cheong, Hong-Hin and Siu, Shirley Weng In},
  booktitle={International Conference on Algorithms for Computational Biology},
  pages={155--166},
  year={2020},
  organization={Springer}
}
```
<br/>
<br/>
<br/>
--------------------<br/>
:construction: Last updated: 17/03/2021
