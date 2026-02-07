🦠 Malaria Parasite Detection from Cell Images Using Deep Learning

🌍 Project Overview

Malaria is a life-threatening parasitic disease that continues to affect millions worldwide, particularly in regions with limited access to expert diagnostic facilities. Microscopic examination of blood smear images remains the gold standard for malaria diagnosis, yet it is time-consuming and dependent on skilled professionals.

This project presents a deep learning–based automated malaria detection system that classifies parasitized and uninfected red blood cells from microscopic images. The solution leverages transfer learning with EfficientNet-B0, enabling accurate, scalable, and computationally efficient medical image classification.

🔬 Dataset Access & Download Instructions

Due to dataset size constraints, the image dataset is not included in this repository.

The dataset used in this project is publicly available and can be downloaded from the official NIH repository:

📥 Dataset Source

Dataset Name: Malaria Cell Images Dataset

Provider: National Institutes of Health (NIH)

Link:
https://ceb.nlm.nih.gov/repositories/malaria-datasets/

📁 Expected Directory Structure

After downloading and extracting the dataset, organize the files as follows:

dataset/
├── Parasitized/
└── Uninfected/


Ensure that the folder names exactly match the structure above before running the notebook.

🧹 Data Quality Assessment & Cleaning

To ensure reliable model training, the following steps were performed:

Detection and removal of corrupted or unreadable images

Validation of image dimensions and formats

Consistency checks for class labels

Elimination of duplicate or invalid samples

🧠 Image Preprocessing & Augmentation
🔹 Preprocessing

Image resizing to match EfficientNet-B0 input requirements

Pixel normalization compatible with ImageNet pre-trained weights

🔹 Data Augmentation

Applied only to the training set:

Random rotations

Horizontal and vertical flips

Mild zoom and brightness adjustments

Augmentations were chosen carefully to preserve medically meaningful features.

🧠 Model Architecture & Training
🔹 Transfer Learning Backbone

Model: EfficientNet-B0

Pre-trained on: ImageNet

Rationale: EfficientNet-B0 provides a strong balance between accuracy and computational efficiency, making it suitable for medical imaging tasks.

🔹 Training Strategy

Binary Cross-Entropy loss

Adam optimizer

Early stopping to prevent overfitting

Model checkpointing based on validation performance

Fine-tuning of deeper layers after initial convergence

📊 Model Evaluation

Evaluation focused on clinically relevant metrics:

Sensitivity (Recall for infected cells)

Specificity (True Negative Rate)

Confusion Matrix

Accuracy and F1-score

ROC-AUC analysis

🛠️ Technology Stack

Python

TensorFlow / Keras

EfficientNet-B0

NumPy

OpenCV

Matplotlib

Google Colab

📁 Repository Structure
├── Malaria_Parasite_Detection.ipynb
└── README.md

🚀 Significance of the Project

This project demonstrates how transfer learning can be effectively applied to medical image analysis, providing an automated and scalable diagnostic aid. By focusing on both performance and efficiency, the system aligns well with real-world healthcare deployment scenarios.

🧾 Conclusion


The developed pipeline addresses real-world challenges in malaria diagnosis by combining robust preprocessing, efficient model design, and clinically meaningful evaluation. This work highlights the growing role of deep learning in enhancing healthcare accessibility and diagnostic accuracy.
