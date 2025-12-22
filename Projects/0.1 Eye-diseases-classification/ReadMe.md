# 👁️ AI Eye Disease Detection

## 📌 Overview
Blindness impairs the lives of millions worldwide, yet many eye diseases are preventable with early detection. This project implements a Deep Learning model to automatically classify retinal fundus images into four diagnostic categories.

## 🧠 Model Architecture
I utilized **Transfer Learning** with the **EfficientNet** architecture (via PyTorch).
- **Pre-trained Weights:** ImageNet
- **Input Resolution:** 224x224 pixels
- **Custom Head:** Adjusted specifically for multi-class classification.

## 📊 Performance
The model was trained on a dataset of 4,000+ images and achieved:
- **Accuracy:** ~87%
- **Framework:** PyTorch & Torchvision


<img width="6034" height="4457" alt="Eye_Disease_Project_Dashboard" src="https://github.com/user-attachments/assets/402799c5-1edf-495c-8d16-360a4d2663d7" />

## 📂 Dataset Classes
The model classifies images into:
1. **Normal**
2. **Cataract**
3. **Glaucoma**
4. **Diabetic Retinopathy**

## 🚀 Key Learnings
- **Data Augmentation:** Random horizontal flips and resizing were crucial to prevent overfitting on the training data.
- **Transfer Learning:** Using EfficientNet allowed the model to converge much faster than training a custom CNN from scratch.

## 🔗 Project Links
- **Kaggle Notebook:** [https://www.kaggle.com/code/abdosorour/eye-diseases-dataset/notebook]# AITronix-AI-Engineering-Internship
# AITronix-AI-Engineering-Internship
