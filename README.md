# Real-Time-Fatigue-Detection-System
A real-time fatigue detection system using computer vision and machine learning to classify fatigue states with high accuracy and low latency. Achieved with the help of a feature extraction and inference pipeline capable of processing over 1000+ frames with ~85% accuracy.

## Overview

This project focuses on developing a real-time drowsiness detection system using MATLAB, Computer Vision, and Deep Learning techniques. The goal is to improve safety in transportation and other high-risk environments by detecting signs of fatigue through facial analysis.

The system uses live webcam input, detects human faces using MATLAB’s `vision.CascadeObjectDetector`, preprocesses facial images, and classifies them into **Tired** or **Not Tired** states using a modified AlexNet convolutional neural network.

This solution provides a non-intrusive, scalable approach for fatigue monitoring without requiring physiological sensors like EEG or ECG.

---

## Key Features

- Real-time face detection using webcam feed
- Face cropping and preprocessing for uniform input
- Modified AlexNet model for binary classification
- Detection of tired vs. non-tired facial states
- MATLAB-based implementation using Computer Vision Toolbox and Deep Learning Toolbox
- Optimized for near real-time performance

---

## Technologies Used

- MATLAB
- Computer Vision Toolbox
- Deep Learning Toolbox
- AlexNet (Modified)
- Viola-Jones Face Detection Algorithm
- CNN-based Binary Classification

---

## System Workflow

1. Capture live video from webcam
2. Detect face using Viola-Jones algorithm
3. Crop and resize face image to 227×227 pixels
4. Preprocess image for consistency
5. Feed image into modified AlexNet
6. Classify subject as:
   - Tired
   - Not Tired

---

## Model Architecture and Modifications (AlexNet)

### Network Adaptation
The original AlexNet architecture (designed for 1000-class ImageNet classification) was modified for a binary classification task: **'tired' vs 'not tired'**.

To adapt the network:
- The final classification layer was replaced with a 2-class softmax layer
- The output layer was modified to compute probabilities for the two classes
- Fully connected layers were fine-tuned to extract features relevant to facial fatigue detection

### Architecture Optimization
To improve suitability for real-time inference:
- Network complexity was reduced for faster prediction
- Layer configuration was optimized to balance accuracy and computational efficiency
- Transfer learning was used to leverage pretrained feature extraction capabilities

---

## Training Configuration

### Dataset
The dataset consists of labeled facial images categorized into:
- **Tired**: Half-closed or closed eyes indicating fatigue  
- **Not Tired**: Open and alert eye states  

Labels were primarily determined based on eye closure percentage.

### Hyperparameters
- **Learning Rate**: 0.001 (for stable convergence)
- **Epochs**: 20 (to balance training depth and overfitting risk)
- **Mini-Batch Size**: 64 (for efficient gradient computation and stable updates)

---

## Experiments and Evaluation

The system was evaluated under controlled conditions including:
- Constant lighting environment  
- Limited and structured dataset  

### Observations
- The model performed well under controlled conditions  
- Performance degraded with increased variability in lighting and facial features  
- Misclassifications were observed in cases such as:
  - Glasses interference  
  - Partial occlusion  
  - Non-uniform lighting conditions  

## Challenges Faced

- Limited dataset diversity
- Misclassification with glasses and lighting variations
- Reduced accuracy with diverse real-world conditions
- Computational delays during high-resolution processing

---

## Future Improvements

- Expand dataset diversity across demographics and environments
- Improve robustness under poor lighting conditions
- Add multi-level tiredness detection instead of binary classification
- Explore lightweight deep learning models for faster deployment
- Improve handling of outliers such as glasses and occlusions
---
