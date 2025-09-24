# Deepfake Video Detection

## 📌 Overview

This project develops a **deep learning pipeline** to automatically classify videos as **real** or **deepfake**. Using the **Google DeepFake Detection Challenge dataset**, our models aim to combat misinformation, identity fraud, and malicious propaganda by detecting manipulated media.

---

## 🎯 Objectives

* Detect and classify videos as **real** or **deepfake**.
* Compare **state-of-the-art architectures**: 3D CNN, EfficientNet (Transfer Learning), and ConvLSTM.
* Achieve **robust generalization** to unseen manipulation techniques.
* Support **fact-checkers and social media platforms** in fighting misinformation.

---

## 🗂 Dataset

* **Source:** [DeepFake Detection Challenge (Kaggle)](https://www.kaggle.com/c/deepfake-detection-challenge)
* Thousands of authentic & manipulated videos.
* Balanced real/fake distribution.

---

## 🏗️ Methodology

### Preprocessing

* Extracted and standardized frames to **224×224** resolution.
* Uniform frame sampling (32–64 frames per video).
* Applied **data augmentation** (cropping, flipping, brightness).

### Models Implemented

* **3D CNN** – Captures spatial + temporal features.
* **EfficientNet + LSTM** – Transfer learning for frame-level features + temporal modeling.
* **ConvLSTM** – Combines CNN for spatial and LSTM for temporal dependencies.

### Training

* **Train/Validation/Test split:** 70% / 15% / 15%.
* Optimizer: Adam / AdamW, Learning rate tuned via grid search.
* Regularization: Dropout (0.3–0.5), Early stopping.

---

## 📊 Results

| Model             | Accuracy | F1-Score |
| ----------------- | -------- | -------- |
| 3D CNN            | 89.8%    | 0.89     |
| ConvLSTM          | 89.0%    | 0.88     |
| EfficientNet+LSTM | 90.5%    | 0.90     |

✅ **EfficientNet + LSTM achieved the best performance**, making it the most robust for deepfake detection.

---

## 🛠️ Tech Stack

* **Python**, **TensorFlow/Keras**, **OpenCV**
* **R** (for EDA)
* **Google DeepFake Detection Dataset**

---

## 👩‍💻 Team

* **Namrata Vijay Mali** – Model evaluation & implementation
* **Mansi Sanjay Bhosle** – Architectures & abstract compilation
* **Upadhyayula Sai Mani Ritish** – Problem statement, dataset selection

---

## 📚 References

* [Google & Jigsaw DeepFake Detection Challenge](https://www.kaggle.com/c/deepfake-detection-challenge)

---

## 🚀 Future Work

* Ensemble models to further boost accuracy.
* Optimize inference time for **real-time detection** (≤5s per video).

---

