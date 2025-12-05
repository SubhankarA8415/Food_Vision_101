# 🍱 Food Vision — EfficientNetB0 (Adam vs Lion Optimizer, *IMP - Colab notebook and pdf uploaded are not viewable directly needs to get downloaded otherwise direct link for notebook in drive is provided at the bottom*)

A deep learning project focused on **food image classification** using transfer learning with **EfficientNetB0**.  
The model was trained and fine-tuned on the **Food101 dataset** to compare the performance of two modern optimizers — **Adam** and **Lion**.

---

## 🧠 Project Overview

This project explores the use of **EfficientNetB0**, a lightweight yet powerful CNN, for classifying **101 types of food images**.

Training was done in **two phases** — Feature Extraction and Fine-Tuning — to ensure stability and good generalization.

**Experiments were conducted using:**
- TensorFlow / Keras  
- Food101 (TensorFlow Datasets)  
- Image Size: **224×224**  
- Callbacks: **TensorBoard**, **ModelCheckpoint**, **ReduceLROnPlateau**

---

## ⚙️ Training Pipeline

| Phase                  | Description                                                   | Epochs | Learning Rate  | Layers Trained   |
| ---------------------- | ------------------------------------------------------------- | ------ | -------------- | ---------------- |
| **Feature Extraction** | Train top dense layers with EfficientNetB0 frozen             | 10     | 0.001 → 0.0005 | Top Layers       |
| **Fine-Tuning**        | Unfreeze last 50 layers for domain-specific adaptation        | 8–10   | 1e-5           | Last 50 Layers   |

---

## ⚡ Model Configurations

---

### 🧩 Model 1 — EfficientNetB0 + **Adam Optimizer**

**Objective:** Build a stable and high-performing food classifier through feature extraction + controlled fine-tuning.

#### 🔢 Results

| Phase              | Train Acc | Val Acc | Val Loss |
| ------------------ | --------- | ------- | -------- |
| Feature Extraction | 0.55      | 0.69    | 1.13     |
| Fine-Tuning        | 0.63      | 0.74    | 0.93     |
| **Final**          | 0.66      | **0.75**| **0.87** |

✅ **Final Test Accuracy:** ~75.5%  
💾 **Model Path:** `/models/food_vision_final_adam_model.keras`

#### 📌 Key Takeaways
- Adam’s adaptive learning enabled smooth & stable convergence  
- Feature extraction established a solid feature base  
- Fine-tuning improved class-specific texture recognition  

---

### 🦁 Model 2 — EfficientNetB0 + **Lion Optimizer**

**Objective:** Evaluate the newly introduced **Lion** optimizer for efficient convergence and higher accuracy.

#### 🔢 Results

| Phase                     | Train Accuracy | Val Accuracy | Val Loss |
| ------------------------  | :------------: | :----------: | :------: |
| Feature Extraction        |      0.51      |     0.66     |   1.54   |
| Fine-Tuning (Epoch 10–18) |      0.74      |     0.79     |   0.79   |
| **Final (Epoch 20)**      |    **0.77**    |   **0.80**   | **0.78** |

✅ **Final Test Accuracy:** ~79%  
💾 **Model Path:** `/models/food_vision_final_lion_model.keras`

#### 📌 Key Takeaways
- Lion optimizer gives smoother updates with minimal oscillation  
- Gradual unfreezing prevents overfitting  
- Achieved **~4% higher accuracy** than Adam under identical configs  

---

## 📊 Comparative Summary

| Optimizer | Final Val Accuracy | Test Accuracy | Test Loss | Remarks                      |
| --------- | ------------------ | ------------- | --------- | ---------------------------- |
| **Adam**  | ~75%               | 75.5%         | 0.88      | Stable, well-generalized     |
| **Lion**  | **~79%**           | **79%**       | **0.78**  | Faster, smoother convergence |

🔹 **Winner:** **Lion Optimizer** — higher accuracy + lower loss.

---

## 🧪 Key Insights

- Gradual layer unfreezing significantly boosts transfer learning performance  
- Both Adam & Lion perform well, but **Lion shows superior fine-tuning stability**  
- EfficientNetB0 is an excellent feature extractor for Food101  

---

## 🚀 Tools & Libraries

- TensorFlow / Keras  
- TensorFlow Datasets (TFDS)  
- NumPy, Matplotlib  
- TensorBoard for experiment tracking  
- Google Colab + Drive for training & storage  

---

## 🏁 Conclusion

The **EfficientNetB0 + Lion optimizer** achieved the best results — **~79% test accuracy** with strong generalization.  
This experiment highlights how **optimizer choice** and **staged fine-tuning** dramatically influence transfer learning performance.

---

## 🔗 <a href="https://colab.research.google.com/drive/1_obIJF8VhGxnkpBbU68GY3YDSbNxbgrT?usp=sharing">Link to notebook</a>

---

## 📞 Contact

**Subhankar Pandit**  
**Full Stack Developer | Backend Engineer | AI/ML | Cloud**  
**GitHub**: https://github.com/SubhankarA8415  
**LinkedIn**: https://linkedin.com/in/subhankar-pandit   
