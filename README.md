<h1 align="center">😴 Real-Time Drowsiness Detection System</h1>

<p align="center">
  <b>AI-powered driver drowsiness detection using OpenCV, Dlib & Face Recognition</b><br>
  <i>Detects eye closure and yawning in real time — and alerts instantly ⚡</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue?logo=python" alt="Python Version"/>
  <img src="https://img.shields.io/badge/OpenCV-4.8-green?logo=opencv" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="License"/>
  <img src="https://img.shields.io/badge/Status-Active-brightgreen" alt="Status"/>
</p>

---

## 🚀 Overview

This project is a **real-time drowsiness detection system** that monitors your **eyes and mouth movements** through a webcam feed.  
It uses facial landmark detection to calculate **Eye Aspect Ratio (EAR)** and **Mouth Aspect Ratio (MAR)** — identifying when a person is **drowsy or yawning**.  
If detected, an **alarm sound** is triggered to wake the person up instantly.

---

## ✨ Key Features

✅ Real-time face tracking using `face_recognition`  
👁️ Detects closed eyes with Eye Aspect Ratio (EAR)  
👄 Detects yawning with Mouth Aspect Ratio (MAR)  
🔔 Beeps when drowsiness is detected  
📸 Displays live feed with score overlay  
🧠 Uses CNN-based facial recognition for accuracy  

---

## 🧠 Tech Stack

| Component | Purpose |
|------------|----------|
| **Python** | Core programming language |
| **OpenCV** | Video stream and image processing |
| **Dlib** | Facial landmark detection |
| **face_recognition** | Facial encoding and detection backend |
| **NumPy / SciPy** | Math and distance calculations |
| **Matplotlib / PIL** | Image visualization |

---

## ⚙️ Setup Instructions

### 1️⃣ Prerequisites
Before running, make sure you have:
- Python **3.8+**
- A working **webcam**
- Installed **Microsoft Visual C++ Build Tools** (Windows only)  
  👉 [Download Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/)

---

### 2️⃣ Installation

Run the following commands in your terminal:

```bash
# Clone the repository
git clone https://github.com/yourusername/Real-Time-Drowsiness-Detection.git
cd Real-Time-Drowsiness-Detection

# (Optional) Create a virtual environment
python -m venv venv
venv\Scripts\activate  # For Windows
# source venv/bin/activate  # For macOS/Linux

# Install required dependencies
pip install cmake
pip install dlib
pip install face_recognition
pip install opencv-python pillow numpy matplotlib scipy

