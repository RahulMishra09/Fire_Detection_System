Fire Detection System using Raspberry Pi

Overview

The Fire Detection System is a real-time monitoring system that detects fire and sends alerts using a Raspberry Pi and a flame sensor. This system is designed for early fire detection in homes, offices, and industrial settings to prevent major hazards.

Features

Real-time fire detection using a flame sensor.

Alerts via buzzer, LED, and email/SMS notifications.

Camera integration for image capture on detection.

Cloud integration for remote monitoring.

Temperature and Smoke sensor integration for enhanced accuracy.

Components Required

Raspberry Pi (any model with GPIO support)

Flame Sensor (IR-based or UV-based)

Temperature Sensor (DHT11/DHT22 or MLX90614)

Smoke Sensor (MQ-2/MQ-7)

Camera Module (optional)

Buzzer and LED

Resistors and connecting wires

Installation and Setup

1. Install Dependencies

Ensure your Raspberry Pi is up to date and install the required Python libraries:

sudo apt update && sudo apt upgrade -y
sudo apt install python3-pip
pip3 install RPi.GPIO
pip3 install smtplib
pip3 install picamera
pip3 install requests

2. Hardware Connections

Connect the components to the Raspberry Pi GPIO pins:

Flame Sensor → GPIO Pin (Input)

Temperature Sensor → GPIO Pin (Input)

Smoke Sensor → GPIO Pin (Input)

Buzzer → GPIO Pin (Output)

LED → GPIO Pin (Output)

Camera Module → CSI port

3. Clone the Repository

git clone https://github.com/your-username/Fire_Detection_System.git
cd Fire_Detection_System

4. Run the Fire Detection Script

python3 fire_detection.py

How It Works

The Raspberry Pi continuously monitors the flame sensor, temperature sensor, and smoke sensor.

If a fire is detected:

The buzzer and LED alert users.

A notification is sent via email/SMS.

The camera captures an image (if integrated).

The data is sent to the cloud for remote monitoring (if enabled).

Future Enhancements

Integration with IoT platforms for real-time data monitoring.

AI-based smoke and fire recognition using computer vision.

Mobile app support for remote notifications.
