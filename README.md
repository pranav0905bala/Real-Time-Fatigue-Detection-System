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

## Project Report

Detailed methodology, experiments, and evaluation are included in the final project report inside the `/report` folder.

---
