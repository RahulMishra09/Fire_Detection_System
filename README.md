# Fire Detection System using Raspberry Pi

## Overview

The Fire Detection System is a real-time monitoring setup that detects fire using a camera module connected to a Raspberry Pi.  
It captures video frames, analyzes them for fire presence, estimates the fire intensity, and sends an email alert if fire is detected.  
This system is designed for early fire warning in homes, offices, and industrial settings.

---

## Features

- Real-time fire detection using a camera and computer vision
- Fire intensity estimation
- Automatic email notifications on fire detection
- Easy setup on any Raspberry Pi with a camera

---

## Components Required

- Raspberry Pi (any model with camera support, e.g., Raspberry Pi 4)
- Raspberry Pi Camera Module (or compatible USB camera)
- Power supply for Raspberry Pi
- Internet connection (WiFi or Ethernet)

---

## Installation and Setup

### 1. Install Dependencies

Make sure your Raspberry Pi is updated and install the required Python libraries:

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3-pip
pip3 install opencv-python
pip3 install numpy
pip3 install smtplib
```

> **Note**: Also enable the camera interface on your Pi by running:
> ```bash
> sudo raspi-config
> ```
> Go to **Interface Options** → **Camera** → **Enable**.

---

### 2. Clone the Repository

```bash
git clone https://github.com/RahulMishra09/Fire_Detection_System.git
cd Fire_Detection_System
```

---

### 3. Run the Fire Detection Script

```bash
python3 fire_detection.py
```

---

## How It Works

- The Raspberry Pi continuously captures frames from the camera.
- Using image processing (color detection in OpenCV), it identifies areas that resemble fire (typically bright orange, red, and yellow hues).
- If fire is detected:
  - The system calculates the **fire intensity** based on the size of the detected fire region.
  - An **email alert** is sent to the configured recipient, including details about the fire intensity.
- The system runs continuously until manually stopped.

---

## Fire Detection Method

- Detect fire-like colors using HSV color space filtering.
- Find contours (blobs) of fire regions.
- Calculate the area of the largest fire blob to estimate intensity.

---

## Future Enhancements

- Attach an image of the fire in the email alert
- SMS alert integration
- Cloud dashboard for monitoring multiple locations
- Voice alert system using speakers

---

## License

This project is open-source and available under the MIT License.

---

## Important Notes

- This project is intended for educational and prototype purposes.
- It should not replace certified fire detection and suppression systems.

