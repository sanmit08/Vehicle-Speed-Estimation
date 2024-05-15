# Vehicle-Speed-Estimation
This project presents a vision-based system designed to measure the speed of vehicles on roads, aiding in the enforcement of traffic laws by detecting over-speeding vehicles. The system leverages camera input and advanced computer vision algorithms to detect, track, and estimate vehicle speeds in real-time, making it a cost-effective alternative to traditional sensor-based methods.

## Features
* Vehicle Detection and Tracking: Uses Fast Retina Key-point (FREAK) and Features from Accelerated Segment Test (FAST) algorithms for efficient feature extraction and vehicle detection.
* Speed Estimation: Estimates vehicle speed based on camera input with an approximate error of 2 km/hr.
* Machine Learning: Employs a voting-based classifier combining seven different classifiers, achieving a high accuracy rate.
* Real-time Processing: Designed for real-time applications with high computational efficiency.

## Algorithms and Methodologies
1. Feature Extraction:
   * FAST Algorithm: Used for corner detection and key point extraction.
   * FREAK Descriptor: Inspired by the human retina, providing efficient feature vector generation.

2. Feature Scaling and Dimension Reduction:
   * Feature vectors are normalized and standardized.
   * K-Means clustering and Principal Component Analysis (PCA) are used for dimension reduction.

4. Classification:
   * Seven classifiers are used: Decision Tree, Random Forest, K-Nearest Neighbor, Support Vector Machine, Logistic Regression, XGBoost, and Naïve Bayes.
   * Random Forest provided the highest accuracy with an F1 score of 88.5%.
   * A voting-based classifier combines predictions for improved accuracy.

5. Vehicle Tracking:
   * Utilizes the dlib library to track detected vehicles, assigning unique IDs and updating their positions in subsequent frames using a correlation function.

6. Speed Estimation:
   * Speed is calculated based on the time taken to travel between two known points in the video.
   * The system uses frame difference and frame rate to compute speed in km/hr.


