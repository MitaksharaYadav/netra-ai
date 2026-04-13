# Netra-AI: Bridging the Diagnostic Gap in Rural Retinal Screening

**Netra-AI** is a deployable deep-learning-powered retinal screening system designed to detect **Diabetic Retinopathy (DR)** severity with near specialist-level agreement using EfficientNet-B5 and explainable AI techniques.

The system enables early-stage detection support for primary healthcare environments where access to ophthalmologists is limited.

---

## 🚀 Live Deployment

Frontend (User Interface):
https://netraai-eight.vercel.app

Backend (AI Inference API):
https://mitakshara-netraai-backend.hf.space/docs

---

## 📊 Performance Benchmarks

| Model | Kappa Score | Agreement Level |
|------|-------------|----------------|
| VGG16 | 0.68 | Substantial |
| ResNet50 | 0.74 | Substantial |
| **Netra-AI (EfficientNet-B5)** | **0.9155** | **Near-Perfect** |

Quadratic Weighted Kappa score of **0.9155** demonstrates strong agreement with expert ophthalmologist grading standards on the APTOS-2019 dataset.

---

## 🧠 Technical Architecture

### 1️⃣ Ben-Graham Preprocessing
Normalizes illumination variations, removes black borders, enhances vessel contrast, and standardizes retinal fundus images to **456×456 resolution** for stable deep-learning inference.

### 2️⃣ EfficientNet-B5 Severity Regression Model
Performs ordinal regression-based prediction across **5 diabetic retinopathy stages**:

- No DR
- Mild NPDR
- Moderate NPDR
- Severe NPDR
- Proliferative DR

Higher-resolution feature extraction improves detection of:

- microaneurysms
- hemorrhages
- vascular leakage
- macular abnormalities

---

### 3️⃣ Test-Time Augmentation (TTA)
Improves prediction stability by averaging outputs across multiple augmented inference passes.

---

### 4️⃣ Grad-CAM Explainability Module
Generates lesion-localization heatmaps highlighting clinically relevant retinal regions to support transparent doctor-assisted diagnosis.

---

### 5️⃣ Retinal Image Validation Layer
Automatically filters:

- non-retinal uploads
- blurred scans
- invalid fundus images

This improves reliability during real-world deployment.

---

## 📂 Dataset

**APTOS-2019 Blindness Detection Dataset**

Total Images:
3,662 retinal fundus scans

Severity Labels:

| Label | Condition |
|------|-----------|
| 0 | No DR |
| 1 | Mild NPDR |
| 2 | Moderate NPDR |
| 3 | Severe NPDR |
| 4 | Proliferative DR |

---

## 🏗 Deployment Architecture

Frontend:
React + TailwindCSS (Vercel)

Backend:
FastAPI inference server (HuggingFace Spaces)

Model:
EfficientNet-B5 severity regression pipeline

Explainability:
Grad-CAM visualization

Preprocessing:
Ben-Graham illumination normalization

---

## ⚡ Inference Performance

Average prediction latency:

≈ 2 seconds per retinal scan

Optimized using:

- Test-Time Augmentation
- EfficientNet compound scaling
- GPU-compatible inference pipeline

---

## 🎯 Project Impact

Netra-AI enables scalable early diabetic retinopathy screening support in:

- rural healthcare centers
- tele-ophthalmology workflows
- mobile retinal camps
- primary diagnostic facilities

The system assists clinicians by providing severity-aware predictions with visual explainability support.

---

## 👩‍💻 Author

**Mitakshara Yadav**  
B.Tech Computer Science Engineering  
Manipal University Jaipur  
Reg No: 23FE10CSE00748
