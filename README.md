# Autonomous-Drone-Based-Plant-Disease-Detection-Using-Machine-Learning-for-Precision-Agriculture
Autonomous drone-based precision agriculture system using Pixhawk 2.4.8 and Raspberry Pi 3B+. Implements MobileNetV2 for real-time weed classification and U-Net for plant disease segmentation (future deployment), enabling intelligent crop monitoring and scalable smart farming solutions.

**Autonomous Drone-Based Plant Disease and Weed Detection**
This project presents an autonomous precision agriculture system that integrates a drone platform with machine learning and embedded systems to detect weeds and plant diseases in crop fields.
The system uses a Pixhawk 2.4.8 flight controller for autonomous navigation and a Raspberry Pi 3B+ for onboard image processing and inference.
**System Architecture**
The overall system architecture consists of four main components:
**Autonomous Drone Platform**
Pixhawk 2.4.8 handles flight control and waypoint-based navigation.
The drone autonomously captures images of crops during flight.
**Onboard Processing Unit**
Raspberry Pi 3B+ is mounted on the drone.
It captures images from the camera and runs the trained machine learning models.
MobileNetV2 performs real-time weed and plant classification.
U-Net is developed for future deployment to perform disease segmentation.
**Local Network Communication**
The Raspberry Pi and laptop are connected via a local network.
SMBD (Samba) protocol is used to share captured images from the drone to the laptop.
This enables real-time or near real-time visualization of images and results on the PC during drone operation.
**Ground Station (Laptop/PC)**
Used for monitoring captured images and inference outputs.
Supports model evaluation, debugging, and result visualization.
**Data Flow:**
Drone Camera → Raspberry Pi (Inference) → SMBD File Sharing → Laptop Visualization

**Machine Learning Models**

**MobileNetV2 (Classification)**

Lightweight model optimized for Raspberry Pi 3B+

Used for weed detection and plant health classification

Enables efficient onboard inference with low computational cost

**U-Net (Segmentation – Future Deployment)**

Designed for pixel-level plant disease segmentation

Enables estimation of affected leaf area and disease severity

Intended for future edge deployment and precision spraying applications

Key Features

Autonomous waypoint-based drone navigation

Real-time weed and plant classification

Disease segmentation model for future use

Local image sharing using SMBD (Samba)

Low-cost and scalable precision agriculture solution

**Technologies Used**

Pixhawk 2.4.8 (Flight Controller)

Raspberry Pi 3B+

MobileNetV2

U-Net

SMBD (Samba Protocol)

Python, OpenCV, TensorFlow / Keras

**Future Work**

Optimize and deploy U-Net on embedded hardware

Integrate automated precision spraying mechanism

Add cloud synchronization and analytics dashboard

Support multiple crops and disease classes
