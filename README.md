🍱 Food Vision — EfficientNetB0 (Adam vs Lion Optimizer)
A deep learning project focused on food image classification using transfer learning with EfficientNetB0.
The model was trained and fine-tuned on the Food101 dataset to compare the performance of two modern optimizers — Adam and Lion — in improving model convergence and accuracy.
________________________________________
🧠 Project Overview
This project explores the use of EfficientNetB0, a lightweight yet powerful convolutional neural network, for classifying 101 types of food images.
The training was performed in two phases — Feature Extraction and Fine-Tuning — to balance generalization, stability, and performance.
The experiments were conducted using:
•	TensorFlow / Keras
•	Food101 dataset (via TensorFlow Datasets)
•	Input Size: 224×224 pixels
•	Callbacks: TensorBoard, ModelCheckpoint, ReduceLROnPlateau
________________________________________
⚙️ Training Pipeline

| Phase                  | Description                                                   | Epochs | Learning Rate  | Layers Trained |
| ---------------------- | ------------------------------------------------------------- | ------ | -------------- | -------------- |
| **Feature Extraction** | Trained only top dense layers with frozen EfficientNetB0 base | 10     | 0.001 → 0.0005 | Top Layers     |
| **Fine-Tuning**        | Unfroze last 50 layers for domain-specific adaptation         | 8–10   | 1e-5           | Last 50 Layers |

________________________________________
⚡ Model Configurations
🧩 Model 1 — EfficientNetB0 + Adam Optimizer
Objective: Build a stable and high-performing food classifier through feature extraction and controlled fine-tuning.
Results:

| Phase              | Train Acc | Val Acc  | Val Loss |
| ------------------ | --------- | -------- | -------- |
| Feature Extraction | 0.55      | 0.69     | 1.13     |
| Fine-Tuning        | 0.63      | 0.74     | 0.93     |
| Final              | 0.66      | **0.75** | **0.87** |

✅ Final Test Accuracy: ~75.5%
💾 Model Path: /models/food_vision_final_adam_model.keras
Key Takeaways:
•	Adam’s adaptive learning ensured smooth and stable convergence.
•	Feature extraction built a strong general base.
•	Fine-tuning refined class-specific textures and boosted validation accuracy.
________________________________________
🦁 Model 2 — EfficientNetB0 + Lion Optimizer
Objective: Evaluate the newly introduced Lion optimizer for efficient convergence and improved accuracy.
Results:

| Phase                     | Train Accuracy | Val Accuracy | Val Loss |
| :------------------------ | :------------: | :----------: | :------: |
| Feature Extraction        |      0.51      |     0.66     |   1.54   |
| Fine-Tuning (Epoch 10–18) |      0.74      |     0.79     |   0.79   |
| **Final (Epoch 20)**      |    **0.77**    |   **0.80**   | **0.78** |

✅ Final Test Accuracy: ~79%
💾 Model Path: /models/food_vision_final_lion_model.keras
Key Takeaways:
•	Lion optimizer provided smoother updates with less oscillation.
•	Gradual unfreezing avoided overfitting and preserved pretrained knowledge.
•	Achieved ~4% higher accuracy than Adam on the same configuration.
________________________________________
📊 Comparative Summary

| Optimizer | Final Val Accuracy | Test Accuracy | Test Loss | Remarks                      |
| --------- | ------------------ | ------------- | --------- | ---------------------------- |
| **Adam**  | ~75%               | 75.5%         | 0.88      | Stable and well-generalized  |
| **Lion**  | **~79%**           | **79%**       | **0.78**  | Faster, smoother convergence |

🔹 Winner: Lion Optimizer — achieved higher accuracy and lower loss with the same architecture and dataset.
________________________________________
🧪 Key Insights
•	Transfer learning with gradual layer unfreezing significantly boosts performance.
•	Both Adam and Lion optimizers perform well, but Lion offers superior fine-tuning stability.
•	EfficientNetB0 remains an excellent backbone for medium-sized image datasets like Food101.
________________________________________
🚀 Tools & Libraries
•	TensorFlow / Keras
•	TensorFlow Datasets (TFDS)
•	NumPy, Matplotlib
•	TensorBoard for experiment tracking
•	Google Colab + Drive for training and model storage
________________________________________
🏁 Conclusion
The EfficientNetB0 + Lion optimizer configuration delivered the best performance on the Food101 dataset, achieving ~79% test accuracy with robust generalization.
This experiment highlights the importance of optimizer selection and staged fine-tuning in transfer learning workflows.

