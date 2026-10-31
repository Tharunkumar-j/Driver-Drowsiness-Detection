#  Driver Drowsiness Detection using YOLOv5  
### Real-Time Driver Safety Monitoring System (Computer Vision Project)

This project demonstrates **driver drowsiness detection in real time** using the YOLOv5 object detection framework.  
It identifies fatigue-related behaviors such as **closed eyes**, **yawning**, and **driver distraction**.  

The implementation is done inside a **Jupyter Notebook** and is based on concepts learned from various online resources and tutorials.

---

## 📌 Table of Contents
- [Overview](#overview)   
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [How It Works](#how-it-works)  
- [Project Structure](#project-structure)  
- [Dataset Details](#dataset-details)  
- [Installation & Setup](#installation--setup)  
- [Running the Project](#running-the-project)  
- [Results](#results)  
- [Future Improvements](#future-improvements)  
- [Credits / References](#credits--references)

---

## 🧩 Overview

This project analyzes the driver’s face in real time to detect:

- 👁️ **Closed Eyes** (sleepiness)  
- 😮 **Yawning**  
- 👀 **Looking Away / Distraction**  
- 🙂 **Normal Awake State**

It uses **YOLOv5**, a fast and accurate deep learning model for object detection.

---

## ⭐ Features

- 💤 Detects closed eyes (fatigue)  
- 😮 Detects yawning  
- 👀 Detects distraction  
- 🎥 Works with webcam & videos  
- ⚡ YOLOv5 real-time inference  
- 📓 Implemented fully in Jupyter Notebook  
- 📊 Visual bounding boxes and labels  

---

## 🛠 Tech Stack

| Component | Technology |
|----------|------------|
| Language | Python 3 |
| Notebook | Jupyter Notebook |
| Deep Learning | PyTorch |
| Object Detection | YOLOv5 |
| Image Processing | OpenCV |
| Visualization | Matplotlib |

---

## ⚙️ How It Works

1. Load trained YOLOv5 weights (`best.pt`)  
2. Capture frames via webcam/video  
3. Run YOLOv5 inference  
4. Detect fatigue indicators  
5. Display bounding boxes and labels  

---

## 📁 Project Structure

Driver-Drowsiness-Detection-using_yolov5/
│── MiniProject.ipynb # Main notebook
│── README.md # Documentation
│── requirements.txt # Dependencies
│── .gitignore
│
├── models/
│ └── best.pt # YOLOv5 weights (not uploaded)
│
├── sample_videos/
│ └── sample_drive.mp4 # Input video
│
├── results/
│ └── output_demo.mp4 # Output after detection
│
└── screenshots/
└── demo.png # Sample result


---

## 🗃 Dataset Details

Dataset includes common facial states:

- Eyes open  
- Eyes closed  
- Yawning  
- Looking away  
- Normal driving  

Trained in YOLO format:

images/train, images/val
labels/train, labels/val
dataset.yaml


Dataset created/collected using:

- Roboflow  
- Kaggle datasets  
- LabelImg (for custom annotations)

---

## 🧪 Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/SuhasRock007/Driver-Drowsiness-Detection-using_yolov5.git
cd Driver-Drowsiness-Detection-using_yolov5

2️⃣ Install dependencies
pip install -r requirements.txt

3️⃣ Download YOLOv5
git clone https://github.com/ultralytics/yolov5

4️⃣ Add trained weights

Place them in:

models/best.pt

▶️ Running the Project
Open the Notebook
jupyter notebook


Open:

MiniProject.ipynb


Run all cells.

Webcam / Video Options
cap = cv2.VideoCapture(0)             # default webcam
cap = cv2.VideoCapture(1)             # external webcam
cap = cv2.VideoCapture("sample_videos/test.mp4")  # video file

📊 Results

Bounding boxes on detected features

Labels such as closed_eyes, yawn, distracted

Real-time video output

🚀 Future Improvements

Add alert system (buzzer / audio warning)

Convert to mobile app

Flask or FastAPI deployment

Jetson Nano / Raspberry Pi real-time deployment

Train with larger dataset

Explore YOLOv8 / transformer-based detectors

📚 Credits / References

This project was implemented for learning purposes with guidance from:

YOLOv5 official repository

YouTube tutorials

Roboflow resources

OpenCV documentation

PyTorch documentation
