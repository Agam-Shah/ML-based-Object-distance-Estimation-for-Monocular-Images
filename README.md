# Object Distance Estimation from Monocular Images 🧠

Machine Learning-based project to estimate the distance of objects in single (monocular) images using YOLOv5 and various regression models.

---

## 📋 Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Project Structure](#project-structure)
7. [Training (Optional)](#training-optional)
8. [Results](#results)
9. [Future Work](#future-work)
10. [Author](#author)

---

## Project Overview

This repository contains code and resources for estimating the absolute distance of detected objects in images using a combination of YOLOv5 for object detection and several Machine Learning and Deep Learning regression models. The approach offers a low-cost alternative to LiDAR and stereo-camera systems.

## Features

* **Object Detection:** YOLOv5 (PyTorch)
* **Feature Extraction:** Normalized bounding-box dimensions + actual object dimensions
* **Regression Models:**

  * Linear, Lasso, Ridge Regression
  * K-Nearest Neighbors (KNN)
  * Support Vector Machine (SVM)
  * Decision Tree & Random Forest
  * Simple Neural Network (SNN)
  * LSTM-based RNN
* **Evaluation Metric:** Mean Absolute Error (MAE)
* Day/night performance testing

## Requirements

* NVIDIA GPU (CUDA-compatible)
* Python 3.9.7
* Anaconda or Miniconda

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
2. **Create and activate Conda environment**

   ```bash
   conda create -n object-dist python=3.9.7
   conda activate object-dist
   ```
3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```
2. In the notebook interface, open `yolov5.ipynb`.
3. Update the image filename in the cell that loads the YOLOv5 model.
4. Run all cells (`Shift + Enter`) to detect objects and estimate distances.
5. Processed images will be saved in the `output_images/` folder.

> **Note:** Mismatched CUDA versions may cause issues.

## Project Structure

```
├── requirements.txt
├── yolov5.ipynb
├── training.ipynb       # >50MB, not included
├── test_images/         # Sample images for inference
├── output_images/       # Generated outputs
└── README.md
```

## Results

* **Best Model:** SVM (MAE ≈ 1.73m)
* **Random Forest:** MAE ≈ 1.96m
* **KNN & SNN:** MAE ≈ 2.1m
* Linear models (Linear/Lasso/Ridge) performed poorly on nonlinear data.

## Future Work

* Expand dataset size and variety
* Add depth-map features and camera metadata (height, angle)
* Explore hybrid ML + DL pipelines

## Author

**Agam Sanjay Shah**
Queen Mary University of London
agammehta93@gmail.com

---

*Thank you for checking out this project! Feel free to raise issues or submit pull requests.*
