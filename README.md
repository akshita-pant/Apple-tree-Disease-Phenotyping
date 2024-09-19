# Apple Tree Disease Detection

## Overview

This project utilizes advanced deep learning techniques to identify diseases in apple trees from images of their leaves. The dataset comprises annotated photos categorized into four classes: "healthy," "multiple_diseases," "rust," and "scab." The goal is to develop a robust model for early disease detection in apple orchards.

## Methodology

### 1. Data Collection and Preprocessing

- **Dataset**: Annotated photos organized into training and test sets. Training labels are extracted from a CSV file with an additional 'label' column for further organization.
- **Preprocessing**: 
  - Standardized image resolution to 256x256 pixels.
  - Applied augmentation techniques such as shear, zoom, horizontal flip, and vertical flip.
  - Utilized `ImageDataGenerator` for splitting the dataset into training and validation subsets.

### 2. Proposed Models

- **CNN (Convolutional Neural Network)**:
  - Architecture: Convolutional layers with pooling followed by dense layers for feature learning and classification.
  - Training: 27 epochs with early stopping callbacks and model checkpointing.
  
- **ResNet**:
  - Architecture: ResNet50 with pre-trained weights. Added a dense layer for final classification.
  - Training: 30 epochs with early stopping callbacks and model checkpointing.
  
- **InceptionNet**:
  - Architecture: Built on InceptionV3 with pre-trained weights. Added a dense layer for classification.
  - Training: 30 epochs with callbacks for performance optimization.

### 3. Results

| Algorithm        | Accuracy | F1 Score |
|------------------|----------|----------|
| CNN              | 0.9173   | 0.9022   |
| InceptionNet_v3  | 0.9476   | 0.9016   |
| ResNet50         | 0.4407   | 0.4127   |

- **Prediction Plots**:
  - Accuracy and F1 Score comparisons.
  - Confusion matrices for each model.
