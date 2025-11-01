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

## 🧩 How It Works

1. The webcam captures **live video frames**.  
2. The system detects your **face** and extracts **facial landmarks** (eyes, mouth, nose, etc.).  
3. It then calculates:  
   - **EAR (Eye Aspect Ratio)** → Detects **eye closure**  
   - **MAR (Mouth Aspect Ratio)** → Detects **yawning**  
4. If thresholds are exceeded:
   - A **“Drowsy” alert** appears on the screen  
   - A **beep alarm** is played  
   - The **drowsiness score** dynamically increases when drowsy and decreases otherwise

---

## 🖼️ Output Preview

| Normal | Drowsy |
|--------|--------|
| 🧍‍♀️ Eyes open, mouth closed | 😴 Eyes closed or yawning |

*(Replace these icons with your own project screenshots)*

---

## 🧪 Console Output Example

```
✅ Found 1 face(s) in the image.
✅ Face encodings extracted successfully.
Eyes closed: True
Yawning: False
Score: 5
⚠️ Drowsy! Alarm Triggered.
```

---

## 🧩 Core Logic

```python
# Eye Aspect Ratio (EAR)
def eye_aspect_ratio(eye):
    A = np.linalg.norm(eye[1] - eye[5])
    B = np.linalg.norm(eye[2] - eye[4])
    C = np.linalg.norm(eye[0] - eye[3])
    return (A + B) / (2.0 * C)

# Mouth Aspect Ratio (MAR)
def mouth_aspect_ratio(mouth):
    A = np.linalg.norm(mouth[2] - mouth[10])
    B = np.linalg.norm(mouth[4] - mouth[8])
    C = np.linalg.norm(mouth[0] - mouth[6])
    return (A + B) / (2.0 * C)
```

### Threshold Conditions
```
EAR < 0.25 → Eyes Closed  
MAR > 0.6  → Yawning  
Score ≥ 5  → Alarm triggers & “Drowsy” displayed
```

---

## 🧰 Requirements

Install dependencies before running:

```bash
pip install opencv-python dlib numpy face_recognition Pillow matplotlib scipy
```

---

## 🚀 Run the Project

1. Clone the repository  
   ```bash
   git clone https://github.com/<your-username>/Real-Time-Drowsiness-Detection-System.git
   cd Real-Time-Drowsiness-Detection-System
   ```

2. Run the script  
   ```bash
   python drowsiness_detection.py
   ```

3. Make sure your webcam is enabled.

---

## 💡 Future Enhancements

- 🚗 Integrate with IoT or in-car camera systems  
- 📱 Add mobile app notifications for alerts  
- 📊 Create a dashboard for real-time driver analytics  
- 🧬 Upgrade to **YOLOv8** or **Mediapipe** for faster detection

---

## 👩‍💻 Author

**Khyati Kumari**  
🎓 B.E. in Computer Science & Engineering – *Chandigarh University*  
📧 21bcs5784@cuchd.in  

🔗 [LinkedIn](https://www.linkedin.com/in/khyatikumari21) | [GitHub](https://github.com/khyatikumari21)

---

## 🪪 License

This project is licensed under the **MIT License**.  
You’re free to use, modify, and distribute it for learning and research.

---

<h3 align="center">⭐ If you found this helpful, don’t forget to give it a star!</h3>
<p align="center">Made with ❤️ by <b>Khyati Kumari</b></p>


