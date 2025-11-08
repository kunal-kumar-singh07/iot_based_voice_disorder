# Intelligent Voice Disorder Detection (AI + IoT)

An end-to-end intelligent system for automated detection of voice disorders such as Amyotrophic Lateral Sclerosis (ALS) and Aryluxation, using advanced signal processing, machine learning, and IoT deployment.

---

## Overview

This project implements a complete pipeline for analyzing pathological voice samples to identify potential vocal disorders. It combines acoustic signal feature extraction (MFCC, jitter, shimmer, HNR) with multiple machine learning classifiers and is optimized for real-time IoT edge deployment using microcontrollers such as ESP32.

---

## Features

- Signal acquisition using I²S digital microphone (INMP441)
- Feature extraction: MFCCs, Energy, Zero-Crossing Rate, Jitter, Shimmer, HNR
- Multiple AI models: Logistic Regression, SVM, Random Forest, Gradient Boosting, XGBoost, and MLP
- Model benchmarking with Accuracy, Precision, Recall, and F1-score comparison
- IoT-ready deployment (ESP32 / TensorFlow Lite Micro)
- Hardware and software architecture diagrams included

---

## Repository Contents

| File / Folder | Description |
|----------------|--------------|
| `AI_Model_Performance_Comparison.png` | Benchmark comparison of all ML models |
| `software architecture.png` | Software pipeline diagram |
| `workflow.png` | Overall system workflow and ML logic |
| `voice_disorder_model_advanced.pkl` | Trained ensemble ML model |
| `voice_disorder_scaler.pkl` | StandardScaler used during preprocessing |
| `voice_disorders_dataset.xlsx` | Base dataset |
| `voice_disorders_dataset_advanced.xlsx` | Extracted feature dataset |
| `main.ipynb` | Jupyter notebook containing full code pipeline |
| `.git/` | Git repository folder |

---

## Model Benchmark Summary

| Model | Accuracy | Precision | Recall | F1-Score |
|:------|:----------|:-----------|:---------|:----------|
| Logistic Regression | 0.91 | 0.92 | 0.91 | 0.91 |
| SVM (RBF Kernel) | 0.87 | 0.89 | 0.87 | 0.85 |
| Random Forest | 0.87 | 0.89 | 0.87 | 0.85 |
| Gradient Boosting | 0.83 | 0.85 | 0.83 | 0.83 |
| XGBoost | 0.90 | 0.91 | 0.90 | 0.90 |
| MLP Neural Net | 0.91 | 0.91 | 0.90 | 0.90 |

---

## Workflow

1. Voice Input: Raw voice signal captured via INMP441 microphone  
2. Preprocessing: Noise filtering and normalization  
3. Feature Extraction: MFCC, jitter, shimmer, HNR  
4. Model Inference: Classification using trained ML models  
5. IoT Integration: Results displayed on OLED or sent to cloud  

Refer to `workflow.png` for visual representation.

---

## Hardware Implementation

**Microcontroller:** ESP32  
**Sensor:** INMP441 (I²S microphone)  
**Connectivity:** Wi-Fi (cloud) / On-device inference (TFLite Micro)  
**Output:** OLED display / LED indicators  

Refer to "System Architecture" diagram for the block layout.

---

## Tech Stack

- **Languages:** Python, C++ (ESP32 firmware)
- **Libraries:** NumPy, SciPy, scikit-learn, XGBoost, Matplotlib, TensorFlow Lite Micro
- **Hardware:** ESP32, INMP441 microphone, OLED display
- **Tools:** Jupyter Notebook, Git, TensorFlow Lite Converter

---

## Project Outcome

- Developed a robust, IoT-integrated diagnostic system for early detection of voice disorders.  
- Achieved up to 91% classification accuracy through multi-model ensemble benchmarking.  
- Designed a hardware-software co-architecture optimized for real-time inference.

---

## Author

**Kunal Kumar Singh**  
Email: singhkunaliitianbusiness1@gmail.com  
GitHub: [kunal-kumar-singh07](https://github.com/kunal-kumar-singh07)

---

## License

This project is licensed under the MIT License.  
It is free to use, modify, and distribute for educational and research purposes.
