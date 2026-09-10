<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:F8BBD0,50:CE93D8,100:B39DDB&height=180&section=header&text=Stroke%20Prediction&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=ANN%20Classifier%20with%20SMOTE%20Balancing&descAlignY=58&descSize=15)

</div>

## Overview

A deep learning classifier that predicts stroke risk from patient health data. Real world stroke datasets are heavily imbalanced, with far fewer positive cases than negative ones, so this project puts as much effort into properly balancing and evaluating the data as it does into the network itself.

## Key Features

### Dense ANN architecture
The classifier is built from Dense layers combined with BatchNormalization and Dropout, tuned specifically to avoid overfitting on a relatively small, imbalanced clinical dataset.

### SMOTE oversampling
Synthetic Minority Oversampling is applied to the training data to address the severe class imbalance between stroke and non stroke cases, rather than relying on class weights alone.

### Careful preprocessing
StandardScaler normalization is applied to numeric features, and categorical features are one hot encoded before training.

### EarlyStopping based training
Training halts automatically once validation performance stops improving, preventing the model from memorizing the minority class after SMOTE augmentation.

### Healthcare appropriate evaluation
Precision, recall and F1 score are reported explicitly, since accuracy alone is a misleading metric for an imbalanced, healthcare critical classification task like this one.


## Tech Stack

<div align="center">
<img src="https://tech-orbit.wontory.dev/api?title=StrokeAI&tech=tensorflow,python,scikitlearn,pandas&size=420&duration=20" alt="tech stack orbit" width="420" />
</div>

TensorFlow and Keras for the ANN, imbalanced-learn for SMOTE oversampling, Scikit-learn for preprocessing and metrics, and Pandas for data handling.

## How It Works

Patient records are cleaned, categorical fields one hot encoded, and numeric fields scaled. SMOTE is applied only to the training split to avoid leaking synthetic samples into validation or test data. The ANN is then trained with EarlyStopping and evaluated using precision, recall and F1.

## Setup and Run

1. Install dependencies with `pip install -r requirements.txt`.
2. Place the stroke prediction dataset CSV in `/data`.
3. Run `python preprocess.py` to clean, encode and scale the data.
4. Run `python train.py` to apply SMOTE, train the ANN, and print the evaluation report.

## Roadmap

- Compare SMOTE against other imbalance techniques such as ADASYN
- Add SHAP based explainability for individual predictions
- Wrap the trained model in a small prediction API

## Status

> **Status:** This repository was scaffolded from the project description on the author's resume. Source code is being migrated and added here in stages. Reach out using the contact links below if you would like early access to the implementation.

## Let's Connect

<div align="center">

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rawish0922@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rawishsarfraz)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Rawishs-2882)
[![Phone](https://img.shields.io/badge/Call-+92--332--8747138-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](tel:+923328747138)

</div>

<div align="center">

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:B39DDB,50:CE93D8,100:F8BBD0&height=80&section=footer)

</div>
