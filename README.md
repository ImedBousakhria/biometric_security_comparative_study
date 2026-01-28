# Face Recognition & Biometric Security – Comparative Study

This repository contains a **complete, reproducible notebook project** for a course in **Biometric Recognition and Security**.  
The goal is to **compare classical and deep learning approaches** for face recognition under **realistic (unconstrained) conditions**, and to analyze their performance in both **identification** and **verification** scenarios.

All experiments, results, interpretations, and discussions are **fully documented inside the notebook**.

---

##  Project Objectives

- Implement and compare **classical descriptors** and **deep learning models** for face recognition
- Evaluate performance in:
  - **Identification** (Who is this person?)
  - **Verification** (Is this the same person?)
- Analyze:
  - Accuracy, ROC curves, AUC, EER, FAR/FRR
  - Impact of face detection (Viola–Jones)
  - Computational cost and real-time constraints
- Discuss:
  - Precision vs speed trade-offs
  - Explainability limits
  - Security threats and countermeasures

---

## 📂 Dataset

- **Name:** Celebrity Face Image Dataset  
- **Source:** Kaggle  
- **Link:** https://www.kaggle.com/datasets/vishesh1412/celebrity-face-image-dataset  

### Dataset characteristics:
- ~17 celebrities
- ~100 images per identity
- Images are **unconstrained**:
  - different outfits
  - complex backgrounds
  - pose and lighting variations
- This makes the dataset **challenging** and realistic for biometric evaluation

---

##  Methods Implemented

### Classical Methods
- **LBP (Local Binary Patterns) + SVM**
- **HOG (Histogram of Oriented Gradients) + SVM**
- Variants **with and without Viola–Jones face cropping**

### Deep Learning Methods
- **DeepFace – Facenet512**
- **DeepFace – ArcFace**
- Pretrained models (no training from scratch)

---

## 📊 Evaluation Protocols

### Identification
- Multiclass classification
- Metric: **Accuracy**

### Verification
- Pair-based evaluation (genuine vs impostor pairs)
- Metrics:
  - ROC curve
  - AUC
  - EER
  - FAR / FRR at EER threshold

Both protocols are clearly explained and implemented in the notebook.

---

##  Key Findings (Summary)

- **HOG consistently outperforms LBP** on unconstrained images
- **Viola–Jones face cropping does not always improve results**
  - Detection failures and misalignment degrade classical descriptors
- **DeepFace models significantly outperform classical methods**
  - More robust to background, pose, and lighting variations
- **Verification and identification behave differently**
  - Verification can appear strong even when multiclass identification is difficult
- Clear **trade-off between speed and accuracy**
  - Classical methods: fast but fragile
  - Deep models: accurate but computationally expensive

All numerical results and interpretations are available directly inside the notebook.

---

## ⏱️ Real-Time Constraints & Security Analysis

The notebook includes dedicated sections discussing:
- Computational costs and suitability for real-time systems
- Edge vs server-side architectures
- Explainability limits of deep models
- Security threats:
  - Spoofing
  - Replay attacks
  - Deepfakes
  - Template compromise
- Possible countermeasures (liveness detection, multimodal biometrics, secure templates)

---
