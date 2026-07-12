# 🍱 Food Vision Big

### Production-Grade Deep Learning Food Image Classification System

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-FF6F00?style=for-the-badge&logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-CNN-D00000?style=for-the-badge&logo=keras)
![Computer Vision](https://img.shields.io/badge/Computer-Vision-00ACC1?style=for-the-badge)
![EfficientNetB0](https://img.shields.io/badge/EfficientNet-B0-43A047?style=for-the-badge)
![Transfer Learning](https://img.shields.io/badge/Transfer-Learning-7B1FA2?style=for-the-badge)
![TensorFlow Datasets](https://img.shields.io/badge/TFDS-Food101-F57C00?style=for-the-badge)
![Deep Learning](https://img.shields.io/badge/Deep-Learning-3949AB?style=for-the-badge)

</p>

---

# 📌 Overview

Food Vision Big is a production-grade Deep Learning image classification system built to recognize **101 food categories** using transfer learning with **EfficientNetB0**.

The project demonstrates a complete computer vision workflow—from large-scale dataset preparation and optimized TensorFlow data pipelines to feature extraction, fine-tuning, optimizer comparison, and model evaluation. Trained on the **Food101** dataset, the system explores how different optimization strategies influence transfer learning performance while maintaining a scalable and production-oriented training pipeline. :contentReference[oaicite:0]{index=0}

The project also compares two modern optimizers—**Adam** and **Lion**—to analyze convergence behavior, model stability, and classification accuracy under identical training configurations.

---

# 🎥 Project Resources

| Resource | Link |
|----------|------|
| 📂 GitHub Repository | Repository Home |
| 🏗️ Architecture Documentation | `docs/Architecture.md` |
| 📄 Project Presentation | `docs/Food-Vision-Big-tm.pdf` |
| 🎥 Public Project Showcase | https://youtu.be/ZqmDicba5pU?si=gqtpQxcwOaJfuyIb |
| 🔒 Complete Technical Demonstration | Available upon request (Recruiters, Interviewers, Collaborators & Technical Discussions) |

---

# 🚀 Key Features

## 🖼️ Dataset Engineering

- Food101 dataset with 101 food categories
- TensorFlow Datasets (TFDS) integration
- Optimized `tf.data` input pipeline
- Parallel data loading and automatic prefetching
- GPU-optimized batch processing
- Large-scale image classification workflow

---

## 🧹 Image Preprocessing Pipeline

- Automatic image resizing (224 × 224)
- Float32 tensor conversion
- Pixel normalization
- Efficient tensor preparation
- Production-ready preprocessing workflow
- Native TensorFlow image operations

---

## 🧠 Deep Learning Pipeline

- EfficientNetB0 transfer learning
- Feature extraction workflow
- Fine-tuning for domain adaptation
- 101-class softmax classification
- TensorFlow/Keras implementation
- Production-oriented training pipeline

---

## ⚙️ Training Optimization

- Adam & Lion optimizer comparison
- Mixed Precision Training
- TensorBoard experiment tracking
- Model checkpointing
- ReduceLROnPlateau scheduler
- GPU-accelerated training

---

## 📊 Model Evaluation

- Optimizer performance comparison
- Training & validation accuracy monitoring
- Loss curve analysis
- Model generalization evaluation
- Comparative performance analysis
- Exportable production models

---

# 🏗️ High-Level System Architecture

The project follows a modular Deep Learning workflow where every stage transforms raw image data into optimized model predictions.

```

Food101 Dataset

↓

TensorFlow Dataset (TFDS)

↓

Image Preprocessing

↓

EfficientNetB0

↓

Feature Extraction

↓

Fine-Tuning

↓

Optimizer Training
(Adam / Lion)

↓

Model Evaluation

↓

101-Class Food Classification

```

A detailed explanation of the complete Deep Learning pipeline, model architecture, optimization strategy, and software engineering design is available in:

📄 **docs/Architecture.md**

---

# 📂 Project Structure

```bash
Food_Vision_101/
│
├── Colab_code/
│   ├── Food_Vision.ipynb
│   └── food-vision.pdf
│
├── Models/
│   ├── Feature_Extraction/
│   ├── Fine_Tune_1/
│   └── Final_Model/
│
├── docs/
│   ├── Architecture.md
│   └── Food-Vision-Big-tm.pdf
│
└── README.md
```

---

# 🧠 Deep Learning Pipeline

The complete workflow follows a structured transfer learning pipeline.

## 1️⃣ Dataset Preparation

- Food101 dataset loading
- TensorFlow Dataset integration
- Efficient dataset management
- Automatic dataset preprocessing

---

## 2️⃣ Data Pipeline

- Parallel data loading
- Image resizing
- Tensor conversion
- Batch generation
- Automatic prefetching
- GPU optimization

---

## 3️⃣ Feature Extraction

- ImageNet pre-trained EfficientNetB0
- Frozen convolutional backbone
- High-level visual feature learning
- Dense classification head training

---

## 4️⃣ Fine-Tuning

- Unfreezing upper EfficientNet layers
- Low learning rate optimization
- Domain-specific feature adaptation
- Improved class discrimination

---

## 5️⃣ Optimizer Comparison

Two optimization strategies were evaluated:

### Adam Optimizer

- Stable convergence
- Adaptive learning rates
- Strong baseline performance
- Reliable generalization

### Lion Optimizer

- Faster convergence
- Improved optimization stability
- Higher classification accuracy
- Better final model performance

---

## 6️⃣ Model Evaluation

The trained models were evaluated using:

- Validation Accuracy
- Validation Loss
- Optimizer Comparison
- Generalization Performance
- Classification Stability

---

# 🏛️ Model Architecture

The project is built around **EfficientNetB0**, a lightweight yet highly efficient Convolutional Neural Network optimized for image classification tasks.

The training architecture follows a transfer learning approach:

```

Input Image (224 × 224)

↓

Image Preprocessing

↓

EfficientNetB0 Backbone
(ImageNet Pre-trained)

↓

Global Average Pooling

↓

Dropout Layer

↓

Dense Classification Layer

↓

Softmax Output

↓

101 Food Categories

```

EfficientNetB0 provides a strong feature extraction backbone while significantly reducing computational complexity compared to traditional CNN architectures.

---

# ⚙️ Training Strategy

Training was performed in two distinct stages to maximize model performance while minimizing overfitting.

## 📌 Stage 1 — Feature Extraction

- Frozen EfficientNetB0 backbone
- Train only the classification head
- Fast convergence
- Stable feature learning
- Reduced computational cost

---

## 📌 Stage 2 — Fine-Tuning

- Unfreeze upper EfficientNet layers
- Lower learning rate
- Domain-specific feature adaptation
- Improved class discrimination
- Better generalization performance

---

## 🔄 Optimization Techniques

The project evaluates two optimization algorithms under identical training conditions.

### Adam Optimizer

- Adaptive learning rates
- Stable convergence
- Reliable optimization
- Strong baseline performance

### Lion Optimizer

- Momentum-based optimization
- Faster convergence
- Smoother parameter updates
- Improved validation performance

Additional training enhancements include:

- Mixed Precision Training
- TensorBoard Logging
- Model Checkpointing
- Learning Rate Scheduling
- GPU-Accelerated Training

---

# 📊 Performance Summary

The project compares two optimization strategies for transfer learning with EfficientNetB0.

| Optimizer | Validation Accuracy | Test Accuracy | Key Observation |
|-----------|--------------------:|--------------:|----------------|
| Adam | ~75% | ~75.5% | Stable convergence with strong generalization |
| Lion | **~79%** | **~79%** | Faster convergence with improved final accuracy |

🏆 **Best Performing Model:** EfficientNetB0 + Lion Optimizer

---

# 🛠️ Technology Stack

## 🖥️ Programming

- Python

---

## 🤖 Deep Learning

- TensorFlow
- Keras
- EfficientNetB0
- Transfer Learning
- Fine-Tuning
- Mixed Precision Training

---

## 👁️ Computer Vision

- TensorFlow Datasets (TFDS)
- Food101 Dataset
- Image Classification
- CNN Architectures

---

## 📊 Data Processing

- NumPy
- Matplotlib
- TensorFlow Data Pipeline

---

## ⚙️ Experiment Tracking

- TensorBoard
- ModelCheckpoint
- ReduceLROnPlateau
- Google Colab

---

# ▶️ Running the Project

## 1️⃣ Clone Repository

```bash
git clone https://github.com/SubhankarA8415/Food_Vision_101.git

cd Food_Vision_101
```

---

## 2️⃣ Install Dependencies

```bash
pip install tensorflow tensorflow-datasets matplotlib numpy
```

---

## 3️⃣ Launch Training Notebook

Open:

```text
Colab_code/Food_Vision.ipynb
```

or upload the notebook to **Google Colab** for GPU-accelerated training.

---

# 🌍 Real-World Applications

Food Vision demonstrates how Deep Learning and Computer Vision can be applied to solve real-world image recognition problems.

Potential applications include:

### 🍽️ Smart Food Recognition

- Automatic food identification
- Digital menu systems
- Restaurant automation

---

### 🥗 Nutrition & Healthcare

- Calorie estimation
- Dietary tracking
- Personalized nutrition assistants

---

### 📱 Mobile AI Applications

- Smartphone food recognition
- Edge AI image classification
- Intelligent camera assistants

---

### 🤖 AI Research & Education

- Transfer learning demonstrations
- Optimizer comparison studies
- Deep Learning experimentation
- Computer Vision education

---

# 🚀 Future Improvements

Potential future enhancements include:

- Vision Transformers (ViTs)
- ConvNeXt architectures
- EfficientNetV2
- Real-time webcam inference
- Mobile deployment using TensorFlow Lite
- ONNX model export
- Cloud deployment
- Explainable AI using Grad-CAM
- Multi-label food recognition

---

# 📚 Documentation

This repository follows a documentation-first approach.

Included documentation:

- ✅ Professional README
- ✅ High-Level System Architecture
- ✅ Project Presentation
- ✅ Public Project Showcase
- ✅ Colab Notebook
- ✅ Trained Models

---

# 🔒 Complete Project Demonstration

A comprehensive technical demonstration of the complete project is available for:

- Recruiters
- Hiring Managers
- Technical Interviewers
- Academic Evaluation
- Professional Collaboration
- Technical Discussions

The complete demonstration includes:

- Complete notebook walkthrough
- Deep Learning pipeline explanation
- Transfer learning strategy
- Model architecture discussion
- Optimizer comparison
- Training workflow
- Experimental observations

Please reach out if you would like access for any of the above purposes.

---

# ⚠️ Disclaimer

This project has been developed for educational, research, and demonstration purposes.

The trained models and experimental results are intended to showcase modern Deep Learning and Transfer Learning techniques using the Food101 dataset and should not be interpreted as production-ready commercial food recognition systems.

---

# 👨‍💻 Developer

## **Subhankar Pandit**

**Software Engineer | Full Stack Developer | Backend Engineering | Artificial Intelligence**

Building intelligent software through scalable backend systems, modern web technologies, and AI-powered applications.

---

# 📬 Connect With Me

- 🌐 **Portfolio:** https://portfolio-subhankar-pandits-projects.vercel.app/
- 💻 **GitHub:** https://github.com/SubhankarA8415
- 💼 **LinkedIn:** https://www.linkedin.com/in/subhankar-pandit-080449255
- 📺 **YouTube:** https://www.youtube.com/@SubhankarDevLab
- 📧 **Email:** subhankar.pandit2002@gmail.com

---

# ⭐ Support the Project

If you found this project useful or interesting, consider giving the repository a ⭐.

It helps support the project and encourages future development of Deep Learning, Computer Vision, and AI-powered software engineering projects.
