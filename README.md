# Deep Learning Road Extraction using DeepLabV3+

## Overview

This repository contains a comprehensive Jupyter notebook (`Road_Extraction_Using_Satellite_Images.ipynb`) that demonstrates the end-to-end process of training a DeepLabV3+ model for road extraction. The model is trained on the DeepGlobe Road Extraction Dataset, and the code is specifically designed to run on Google Colab.

## Getting Started
![image](https://github.com/Ali-Hasan-Khan28/Deep-Globe-Road-Extraction-Using-Deep-Learning/assets/101451471/111c4ab1-7fd3-446c-b236-4a2a69063590)


### Prerequisites

- Python
- Jupyter Notebook
- Required Python libraries (install using `pip install -r requirements.txt`)

### Kaggle API Setup

Before running the code, make sure to set up your Kaggle API credentials. Upload the Kaggle API key as instructed in the notebook. This step is crucial for downloading the DeepGlobe Road Extraction Dataset.

### Dataset Download

The notebook utilizes the Kaggle API to download the [DeepGlobe Road Extraction Dataset](https://www.kaggle.com/datasets/balraj98/deepglobe-road-extraction-dataset). Replace the placeholder with your Kaggle username and key.

## Data Preprocessing

The code includes functions for thorough data preprocessing. This involves:
- Shuffling the dataset
- Augmentation (Horizontal and Vertical Flip)
- One-hot encoding of masks

## Model Architecture

The notebook employs the DeepLabV3+ architecture with a ResNet50 encoder pre-trained on ImageNet. The model is configured for road extraction, with the training objective defined by the Dice Loss. Evaluation is performed using Intersection over Union (IoU) score.

![image](https://github.com/Ali-Hasan-Khan28/Deep-Globe-Road-Extraction-Using-Deep-Learning/assets/101451471/5e1ce471-62a0-40df-b1fd-f94dcbb32fa1)


## Training

The training process is controlled by the `TRAINING` variable. If set to `True`, the model will be trained for the specified number of epochs. The best model is saved based on the highest IoU score on the validation set.

## Inference and Visualization

The notebook includes an inference section where the trained model is loaded, and predictions are generated for a subset of the validation dataset. Visualization includes original images, ground truth masks, and predicted masks. This provides an intuitive understanding of the model's performance.

## Evaluation

The notebook evaluates the model on the test dataset, presenting metrics such as Mean IoU Score and Mean Dice Loss. These metrics give insights into the model's effectiveness in road extraction.

## Results

The repository generates two key plots to visualize the model's performance over epochs:
- `iou_score_plot.png`: Plot of IoU Score
- `dice_loss_plot.png`: Plot of Dice Loss

![image](https://github.com/Ali-Hasan-Khan28/Deep-Globe-Road-Extraction-Using-Deep-Learning/assets/101451471/a2f7b5c7-5adf-4d58-91ff-cede3905cf41)


![image](https://github.com/Ali-Hasan-Khan28/Deep-Globe-Road-Extraction-Using-Deep-Learning/assets/101451471/8d7c7a83-c9e1-46f3-bf92-369b4365a29c)


## Author

Ali Hasan Khan

