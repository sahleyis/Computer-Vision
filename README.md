# 🌌 VisionNexus: Multi-Modal CV & Biometric Gateway

**VisionNexus** is a real-time computer vision suite built with OpenCV and MediaPipe. Developed within the **Google Antigravity IDE**, this project bridges the gap between simple motion tracking and advanced biometric security.

---

## 🎯 Project Overview
This application performs simultaneous tracking of colors, hands, and body poses. It utilizes a Machine Learning pipeline to classify landmarks and is currently evolving toward a **Face Verification** system for local application authentication.



## ✨ Core Features
* 🌈 **Dynamic Color Detection:** Uses HSV color space masking to isolate and track specific objects.
* ✋ **Hand Landmark Mapping:** 21-point skeletal tracking for precise gesture recognition.
* 🧍 **Full-Body Pose Estimation:** Differentiates between limbs and joints using the MediaPipe Holistic model.
* 🧠 **ML Classification:** A training pipeline that learns to distinguish between specific user-defined postures and parts.
* 🔐 **Biometric Roadmap:** Future integration of FaceNet for "Gatekeeper" app access.

---

## 🛠️ Technical Stack
| Component | Technology |
| :--- | :--- |
| **Language** | Python 3.10+ |
| **Vision Engine** | OpenCV |
| **Landmark Logic** | MediaPipe |
| **ML Training** | Scikit-learn / TensorFlow |
| **IDE** | Google Antigravity |
| **Agent** | Claude Opus 4.6 |

---

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have a working webcam and Python installed.

### 2. Installation
```bash
pip install opencv-python mediapipe numpy scikit-learn
