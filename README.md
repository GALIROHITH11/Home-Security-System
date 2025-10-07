[README.md](https://github.com/user-attachments/files/22744774/README.md)
# 🏠 Home Security System

A **computer vision–based home security system** that detects and recognizes faces in real time using **OpenCV** and **LBPH (Local Binary Patterns Histograms)**. It enhances home safety by distinguishing between authorized and unknown individuals and sends **instant SMS alerts** via **Twilio API** when an intruder is detected.

---

## 📘 Table of Contents
- [Overview](#overview)
- [Objectives](#objectives)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Hardware & Software Requirements](#hardware--software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Modules](#modules)
- [Results](#results)
- [Future Enhancements](#future-enhancements)
- [Contributors](#contributors)
- [License](#license)

---

## 🧠 Overview
Traditional home security systems often fail to distinguish between known and unknown individuals, leading to false alarms.  
This project introduces a **smart home security system** that integrates **facial recognition, automation, and alert mechanisms** to detect, recognize, and notify homeowners about intrusions in real time.

---

## 🎯 Objectives
- To detect and recognize faces using computer vision.
- To distinguish between authorized and unauthorized persons.
- To send SMS alerts when an unknown face is detected.
- To maintain a secure, automated, and scalable home surveillance system.

---

## ✨ Features
- Real-time **Face Detection** using Haar Cascade.
- **Face Recognition** with LBPH algorithm.
- **SMS Notifications** for unknown faces via Twilio.
- Saves detected faces with **timestamps**.
- Works on **PC or Raspberry Pi** with camera input.

---

## 🧩 System Architecture
The system has three major layers:
1. **Input Layer:** Captures live video feed using a webcam or CCTV.
2. **Processing Layer:** Detects and recognizes faces using OpenCV and trained LBPH model.
3. **Output Layer:** Displays live feed and sends SMS alerts using Twilio API.

---

## ⚙️ Hardware & Software Requirements

### Hardware
- PC / Laptop / Raspberry Pi  
- Webcam or CCTV Camera  
- Internet connection for SMS alerts  

### Software
- **OS:** Windows / Linux / Raspberry Pi OS  
- **Language:** Python 3.7+  
- **Libraries:**
  ```bash
  opencv-python
  opencv-contrib-python
  numpy
  twilio
  ```

---

## 💻 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/HomeSecuritySystem.git
   cd HomeSecuritySystem
   ```

2. Install dependencies:
   ```bash
   pip install opencv-python opencv-contrib-python numpy twilio
   ```

3. Create a folder named `dataset/` and add authorized face images.

4. Update your Twilio credentials in the script:
   ```python
   TWILIO_PHONE_NUMBER = "+1XXXXXXXXXX"
   TWILIO_ACCOUNT_SID = "your_account_sid"
   TWILIO_AUTH_TOKEN = "your_auth_token"
   ```

---

## ▶️ Usage

1. Train the recognizer:
   ```bash
   python train_recognizer.py
   ```

2. Run the real-time recognition:
   ```bash
   python home_security.py
   ```

3. Press `q` to quit the live surveillance window.

---

## 🧱 Modules

| Module | Description |
|---------|--------------|
| Face Detection | Detects faces using Haar Cascade. |
| Face Recognition | Identifies known faces using LBPH recognizer. |
| Alert Mechanism | Sends SMS via Twilio when unknown faces are detected. |
| Image Logging | Stores captured images with timestamped filenames. |

---

## 📊 Results

- **Training Accuracy:** 83.4%  
- **Validation Accuracy:** 70.82%  
- **Real-Time Response:** Instant SMS alert upon unknown face detection.  

Sample workflow:
1. System initializes → Loads trained model  
2. Detects faces in live feed  
3. Recognizes authorized users  
4. Sends SMS alert for unknown faces  
5. Saves snapshot with timestamp  

---

## 🚀 Future Enhancements
- Integration with **smart locks and IoT devices**.  
- Use of **deep learning models** (FaceNet, Dlib CNN).  
- Cloud-based **data storage and mobile app control**.  
- Low-light and occlusion robustness improvements.  

---

## 👨‍💻 Contributors
- **G. Rohith** (BU22CSEN0600072)  
- **P. Surendra** (BU22CSEN0600049)  
- **G. Ranjith Kumar** (BU22CSEN0600060)  
- **S. B. Jeevan** (BU22CSEN0600197)  

**Department of Computer Science and Engineering**  
GITAM School of Technology, Bengaluru Campus  

---

## 📜 License
This project is developed as part of an academic mini-project for **OOSE-Based Application Development Lab (CSEN2091P)**.  
Usage for educational and research purposes is encouraged.
