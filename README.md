# SightGuard: Real-Time Object Detection and Localization for Enhanced Navigation

## Project Overview

SightGuard is an advanced assistive technology system designed to enhance the navigation capabilities of visually impaired individuals. Utilizing real-time object detection and localization, SightGuard provides immediate feedback on the user's surroundings, enabling safer and more confident mobility. The system is built on a combination of powerful hardware, intelligent software, and mobile integration.

## Features

- **Real-Time Object Detection**: Identifies and localizes objects in the user's environment in real-time.
- **Distance Estimation**: Provides approximate distances to detected objects to help users avoid obstacles.
- **User-Friendly Mobile App**: Interfaces with a mobile application for easy access to real-time data and navigation instructions.
- **Portable and Efficient**: Designed to be lightweight and efficient, making it suitable for everyday use.

## Hardware Components

1. **Raspberry Pi 0 W with API (4B Protocol)**
   - Acts as the core processing unit, running the YOLOv3 model for object detection and localization.
   - Utilizes the Raspberry Pi 4B protocol for efficient data handling and processing.

2. **Camera OV 5647 No 2R WebCAM**
   - Captures real-time video feed for processing.
   - Provides high-resolution imagery necessary for accurate object detection.

## Software Components

1. **Flask Server**
   - A lightweight web server that handles API requests from the mobile application.
   - Processes and relays data between the Raspberry Pi and the mobile app for real-time interaction.

2. **Mobile Application**
   - Provides an interface for users to receive real-time feedback on detected objects and their distances.
   - Designed with accessibility in mind, offering voice feedback and intuitive controls.

3. **SolidWorks and PROTEUS Software**
   - **SolidWorks**: Used for designing and simulating the mechanical components of the system, ensuring a compact and ergonomic design.
   - **PROTEUS**: Employed for circuit design and simulation, allowing for efficient hardware integration and testing.

4. **YOLOv3**
   - A state-of-the-art object detection algorithm used to identify and localize objects within the camera's field of view.
   - Optimized for running on the Raspberry Pi, providing a balance between accuracy and performance.

## Methodology

1. **Hardware Setup**:
   - The Raspberry Pi 0 W, connected to the Camera OV 5647, captures live video feed. The camera is positioned to mimic the user's line of sight, ensuring accurate detection of obstacles.

2. **Object Detection and Localization**:
   - The YOLOv3 model, running on the Raspberry Pi, processes each video frame in real-time. It identifies objects, their positions, and calculates distances based on the size of the objects in the frame.

3. **Data Transmission**:
   - The processed data is sent to a Flask server running on the Raspberry Pi. The server acts as a middleware, handling API requests from the mobile application.

4. **Mobile Application**:
   - The mobile app receives the data and presents it to the user through a simple interface. The app provides both visual and auditory feedback, helping the user navigate their surroundings safely.

5. **Design and Simulation**:
   - SolidWorks is used to design the enclosure and any mechanical parts required for the system. PROTEUS is utilized to simulate the electronic circuitry before physical implementation.

## Installation and Setup

### Prerequisites

- Raspberry Pi 0 W with Raspbian OS installed
- Camera OV 5647 No 2R WebCAM connected to the Raspberry Pi
- Python 3.x installed on Raspberry Pi
- Flask and necessary Python packages (refer to `requirements.txt`)
- Mobile device with the SightGuard mobile app installed

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/sightguard.git
   cd sightguard
