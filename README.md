# 🧠 Object Distance Estimation from Monocular Images using Machine Learning

This project implements a Machine Learning-based approach to estimate the distance of an object from a single (monocular) image using object detection and regression models. The methodology leverages YOLOv5 for object detection and various ML/DL models to predict distance based on object bounding box dimensions and actual object sizes.

## 📚 About the Project

Traditional distance estimation systems rely on expensive hardware like LiDAR or stereo cameras. This research provides an affordable alternative by:
- Using monocular RGB images
- Extracting object features from YOLOv5 bounding boxes
- Applying machine learning models for regression-based distance estimation

## 🔍 Key Features
- **YOLOv5** for real-time object detection
- Feature vector extraction: `[1/Bw, 1/Bh, 1/Bd, Ch, Cw, Cb]`
- Regression models used:
  - Multiple Linear Regression
  - Lasso & Ridge Regression
  - K-Nearest Neighbors (KNN)
  - Decision Tree & Random Forest
  - Support Vector Machine (SVM)
  - Simple Neural Network (SNN)
  - Long Short-Term Memory (LSTM)

## 🏆 Results Summary
- **Best Performing Model:** SVM with MAE ≈ **1.73m**
- **Other Notables:** Random Forest, KNN, and SNN performed decently.
- **Poor Performers:** Linear, Ridge, Lasso (due to data non-linearity)
- **Challenges:**
  - Low dataset size (1797 entries)
  - Poor performance on close-proximity objects
  - Manual labeling introduced noise

## 📁 Dataset
- RGB images from [2]
- Manual annotations using YOLOv5
- Bounding box normalization to reduce resolution bias
- Classes used: `car`, `person`, `bicycle`

## 🔧 Tech Stack
- Python
- PyTorch
- OpenCV
- Scikit-learn
- TensorFlow / Keras (for SNN, LSTM)
- YOLOv5 (PyTorch version)

## 📈 Performance Metrics
- **Mean Absolute Error (MAE)** for validation and test sets
- Visual analysis using error bins and distance comparisons in day/night conditions

## 📷 Sample Use Cases
- Autonomous vehicles
- Surveillance and robotics
- Navigation for visually impaired assistance systems

## 📌 Future Work
- Collect larger and more varied datasets
- Incorporate depth maps and camera metadata (angle, height)
- Explore hybrid ML + DL approaches with real-world deployment potential

## 👨‍🎓 Author

**Agam Sanjay Shah**  
School of Electronic Engineering and Computer Science  
Queen Mary University of London  
📧 agammehta93@gmail.com

---


