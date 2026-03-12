#  Autonomous UAV Fire Detection and Alert System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-DeepLearning-red)
![YOLOv11](https://img.shields.io/badge/YOLOv11-ObjectDetection-green)
![AirSim](https://img.shields.io/badge/AirSim-DroneSimulation-orange)
![Unreal Engine](https://img.shields.io/badge/UnrealEngine-4.27-black)
##  Overview

This project presents an **Autonomous UAV-based Fire Detection and Alert System** developed using **computer vision and drone simulation technologies**. The system integrates a **YOLOv11 deep learning model** with a simulated UAV environment to detect fire and smoke in real time.

A drone patrols a forest environment created in **Unreal Engine 4.27** using the **Microsoft AirSim simulator**. The UAV continuously captures video frames from its onboard RGB camera and processes them using the trained detection model.

When fire or smoke is detected above a predefined confidence threshold, the system automatically generates an **alert with GPS coordinates and detection confidence**, enabling faster emergency response.

This solution demonstrates how **AI-driven UAV surveillance systems can significantly improve wildfire monitoring and early detection**.

---

##  Key Features

- Autonomous UAV surveillance using AirSim simulation  
- Real-time **fire and smoke detection using YOLOv11**
- Integration with **Unreal Engine 4.27 forest environment**
- Autonomous patrol using **Coverage Path Planning (CPP)**
- Dynamic route adjustment using **A* path planning**
- Real-time **fire alert system with GPS location logging**
- Performance evaluation across **multiple environmental conditions**

---

##  System Architecture

```
UAV RGB Camera
      │
      ▼
Image Capture from AirSim
      │
      ▼
YOLOv11 Fire & Smoke Detection
      │
      ▼
Confidence Threshold Check
      │
      ▼
Fire Alert System
      │
      ▼
GPS Coordinates + Detection Confidence
```

---

##  Technologies Used

| Technology | Purpose |
|------------|--------|
| Python | Core programming language |
| YOLOv11 | Fire and smoke detection |
| PyTorch | Deep learning framework |
| OpenCV | Image processing |
| Microsoft AirSim | UAV simulation environment |
| Unreal Engine 4.27 | 3D forest simulation |
| Roboflow | Dataset preparation and annotation |

---

##  Project Structure

```
autonomous-uav-fire-detection
│
├── README.md
├── requirements.txt
│
├── model
│   └── yolov11_fire_detection.pt
│
├── src
│   ├── fire_detection.py
│   ├── drone_camera_stream.py
│   └── alert_system.py
│
├── simulation
│   ├── airsim_setup.md
│   ├── unreal_environment.md
│   └── weather_testing.md
│
├── evaluation
│   ├── results.md
│   ├── confusion_matrix.png
│   └── precision_recall_curve.png
│
└── media
    ├── drone_simulation.png
    ├── fire_detection_example.png
    └── system_architecture.png
```

---

##  Model Performance

| Metric | Value |
|------|------|
| mAP@0.5 | **0.769** |
| Average Precision (Fire) | **0.834** |
| Average Precision (Smoke) | **0.704** |
| Peak F1 Score | **0.76** |

---

##  Environmental Testing

The system was evaluated under different simulated weather conditions:

| Condition | Average Confidence | Observation |
|-----------|------------------|-------------|
| Normal Weather | **0.79** | Highest detection accuracy |
| Rain | **0.69** | Slight visibility impact |
| Snow | **0.59** | Moderate performance |
| Dust Storm | **0.47** | Reduced detection confidence |
| Fog | **0.41** | Most challenging scenario |

These results demonstrate how **environmental visibility significantly affects vision-based fire detection systems**.

---

##  Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/autonomous-uav-fire-detection.git
cd autonomous-uav-fire-detection
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

##  Running Fire Detection

Run the fire detection script:

```bash
python src/fire_detection.py
```

This script loads the trained YOLO model and performs **real-time fire detection on video frames**.

---

##  Fire Alert Logic

The alert system triggers when detection confidence exceeds a predefined threshold:

```python
if confidence > 0.5:
    trigger_fire_alert(gps_location, confidence)
```

Alerts include:

- Fire detection confidence
- UAV GPS coordinates
- Timestamp of detection

---

##  Example Output

Example detection output showing fire and smoke bounding boxes detected by the model.

![Fire Detection](media/fire_detection_example.png)

---

##  Future Improvements

- Multi-drone collaborative wildfire monitoring
- Sensor fusion (thermal + RGB cameras)
- Adaptive confidence thresholds for low visibility
- Real-world UAV deployment

---

## 👩‍💻 Author

**Vidhi Singh**

Computer Science Engineer  
AI | Computer Vision | Autonomous Systems

---
