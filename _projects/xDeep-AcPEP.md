---
title: "xDeep-AcPEP"
image: 
  path: /assets/img/project_acp/acpep_logo_sm.png     
  thumbnail: /assets/img/project_acp/acpep_logo.png   
  caption: ""
---

### Deep Learning Method for Anticancer Peptide Activity Prediction based on Convolutional Neural Network and Multi-Task Learning

##### :fire: Online prediction server is available at: [xDeep-AcPEP on CBBio](https://app.cbbio.online/acpep/home) :fire:
##### :beginner: More details could be found at: [Here](https://app.cbbio.online/acpep/method)

### 1. What's xDeep-AcPEP ?
<p>xDeep-AcPEP is a novel regression method based on convolutional neural network and multi-task learning to predict the bioactivity of anticancer peptides. A set of cancer-specific models were trained using the CancerPPD data sets to predict for six tumor cells: breast, colon, cervix, lung, skin, and prostate.</p>

### 2. How this model was developed？
<p>As shown in the workflow figure (Figure 1), we chose the following 4 descriptors to describe a sequence into numerical form: AAINDEX (AAI), BLOSUM62 (BLO), Z-scale descriptor (ZSC) and Binary profile (BIN). The encoder contains two 1D-convolutional layers with ReLU, two average pooling layers, two batch normalization layers and one max pooling layer. The regressor contains three fully connected layers with one final output neuron. We define the applicability domain (AD) of each model to allow estimation of the uncertainty in the prediction for an unknown instance. The Euclidean distance between an instance and the centroid of the training data in the feature space is measured. If the instance is within a pre-defined cutoff (Z), then prediction can be made with confidence.</p>

If this server helped you, please cite the following paper:
# COMING SOON !
<br/>
<br/>
<br/>
--------------------<br/>
:construction: Last updated: 25/06/2021
