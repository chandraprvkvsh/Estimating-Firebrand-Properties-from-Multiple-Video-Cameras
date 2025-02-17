# Estimating Object Properties from Multi-Angle Images  

Welcome to the **Estimating Object Properties from Multi-Angle Images** project! This project focuses on estimating various characteristics of an object using only images taken from four different angles. By leveraging Convolutional Neural Networks (CNNs), we aim to classify object shapes and predict key physical properties such as dimensions, orientation, surface area, and volume.  

## Background  

Understanding object properties from images is a crucial challenge in computer vision, with applications in various fields such as robotics, industrial automation, and scientific analysis. In this project, we trained models to estimate object properties from images taken by a system of **four video cameras**, simulating real-world multi-view analysis.  

For our specific case study, we applied this method to **firebrands**—small pieces of burning material generated during wildland fires. Firebrands can travel long distances and ignite vegetation or structures, contributing to fire spread. By analyzing firebrands, we can better understand their role in wildfires.  

## Project Overview  

We approach this problem in two stages:  

1. **Shape Classification:**  
   - We first classify the object’s shape using CNNs.  
   - We train custom CNN models and fine-tune **pretrained networks** like **VGG-16, ResNet-50, MobileNet, and DenseNet**, training only the last few layers.  
   - **Early stopping** is used to prevent overfitting, and a **confusion matrix** is plotted to evaluate classification performance.  

2. **Regression for Physical Properties:**  
   - We predict **length, width, height, orientation (Euler angles: roll, pitch, yaw), surface area, and volume** using CNN-based regression.  
   - Features are extracted from images and passed through dense layers to estimate these properties.  
   - Different models are used for different physical attributes.  

## Model Interpretability  

To understand **what the model is learning**, we employ:  

1. **Saliency Mapping:**  
   - Saliency maps highlight the most important pixels influencing the model’s decision.  
   - By computing gradients of the predicted class with respect to input pixels, we visualize which parts of the image contribute the most to classification.  

2. **Grad-CAM (Gradient-weighted Class Activation Mapping):**  
   - Grad-CAM generates heatmaps showing which regions influence the model’s decision-making process.  
   - Unlike saliency maps, Grad-CAM uses the final convolutional layers to highlight **spatially important regions** that led to a prediction.  

These techniques help us ensure the model is making decisions based on meaningful object features rather than irrelevant background patterns.  

## Dataset  

We trained our models using a **synthetic dataset of firebrand images**. The dataset consists of images captured from four different angles to ensure comprehensive object characterization. You can find the dataset [here](https://drive.google.com/file/d/10H3ohDJTGproNjZPn0SBZhzTwMjuUd6w/view?usp=sharing).  

## Note  

1. We initially tackle the classification problem to determine the shape of the firebrands, as this information is necessary for approaching the regression problem.  
2. The original dataset is used for the classification task, and then three CSV files are exported for use in the regression problem.  
3. If GitHub doesn't render the Python notebooks, please download them and run locally, as all experiments were conducted within the notebooks, making them quite large.

