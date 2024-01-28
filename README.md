# Deep Learning Road Extraction using DeepLabV3+

## Overview

This repository contains a Jupyter notebook (`DNN_ALL_CODE.ipynb`) showcasing the implementation of a DeepLabV3+ model for road extraction using the DeepGlobe Road Extraction Dataset. The code is designed for Google Colab and covers key steps such as data download, preprocessing, model training, and evaluation.

## Getting Started

### Prerequisites

- Python
- Jupyter Notebook
- Required Python libraries (install using `pip install -r requirements.txt`)

### Kaggle API Setup

Before running the code, set up your Kaggle API credentials. Upload the Kaggle API key as instructed in the notebook.

### Dataset

The code downloads the [DeepGlobe Road Extraction Dataset](https://www.kaggle.com/datasets/balraj98/deepglobe-road-extraction-dataset) using the Kaggle API. Replace the placeholder with your Kaggle username and key.

## Data Preprocessing

Functions for data preprocessing include shuffling, augmentation, and one-hot encoding of masks.

## Model Architecture

The notebook uses the DeepLabV3+ architecture with a ResNet50 encoder pre-trained on ImageNet. Training employs the Dice Loss, and evaluation is based on Intersection over Union (IoU) score.

## Training

The training process is controlled by the `TRAINING` variable. If set to `True`, the model will be trained for the specified number of epochs. The best model is saved based on the highest IoU score on the validation set.

## Inference and Visualization

The trained model is loaded for inference on a subset of the validation dataset. Visualization includes original images, ground truth masks, and predicted masks.

## Evaluation

Evaluation metrics on the test dataset are provided, including Mean IoU Score and Mean Dice Loss.

## Results

Plots of IoU Score and Dice Loss over epochs are generated and saved as `iou_score_plot.png` and `dice_loss_plot.png`.

## Author

[Your Name]

## Acknowledgments

- The code is adapted from a Kaggle competition and uses the `segmentation-models-pytorch` library.

