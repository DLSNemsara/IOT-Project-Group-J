# Driver Drowsiness Monitoring System (DMS)

## Overview
The Driver Drowsiness Monitoring System (DMS) is an IoT-based solution designed to enhance road safety by detecting driver drowsiness in real-time. The system uses hardware components such as the ESP32 microcontroller, ESP32-CAM module, and GPS-NEO-6M module, alongside cloud services like Firebase and ThingSpeak for data storage and visualization. The system captures driver face images and vehicle location to detect drowsiness, and it provides real-time monitoring via a web dashboard.

This project was completed as part of the **PUSL2022 - Introduction to IoT** module at the **University of Plymouth**.

## Key Components
- **ESP32 Microcontroller**: Central control unit for coordinating modules.
- **ESP32 CAM Module**: Captures driver face images for drowsiness detection.
- **GPS-NEO-6M Module**: Tracks vehicle location and speed.
- **Firebase Realtime Database**: Logs vehicle data and drowsiness events.
- **ThingSpeak**: Cloud platform for real-time data visualization.
- **Web Interface**: Dashboard for visualizing real-time data.

## System Architecture
1. **Hardware**: 
   - ESP32 Microcontroller
   - ESP32 CAM Module
   - GPS-NEO-6M Module
2. **Software**: 
   - Firebase for backend management
   - ThingSpeak for real-time monitoring
   - Web-based dashboard with HTML, CSS, and JavaScript

3. **Data Flow**:
   - Data is captured from sensors (GPS, camera) by the ESP32.
   - Drowsiness detection is performed locally on the ESP32-CAM images.
   - Data is logged to Firebase and visualized in ThingSpeak.

## Database Design
- **Schema**:
  - **drowsiness_events**: Stores event details.
  - **Child Nodes**: Each event contains:
    - `latitude`: Vehicle’s latitude.
    - `longitude`: Vehicle’s longitude.
    - `speed`: Vehicle’s speed.
    - `timestamp`: Event time.

## Deployment
- **Hybrid Hosting**: Combines on-premises servers and cloud services (Firebase, ThingSpeak) for real-time data storage and visualization.
- **Infrastructure**: Includes servers, virtualization for resource optimization, and seamless networking.

## Testing
- **Unit Testing**: Validates individual components (ESP32, sensors, backend).
- **Integration Testing**: Verifies interactions between hardware, cloud services, and dashboard.
- **System Testing**: Ensures end-to-end functionality.

## Dependencies
- **Libraries**: 
  - OpenCV, dlib for facial detection and drowsiness monitoring.
  - Firebase Admin SDK, ThingSpeak API for cloud interaction.
  - Arduino libraries for Wi-Fi, HTTPClient, and sensor control.
- **External Files**:
  - Model files, alarm sounds, HTML for dashboard, Firebase credentials.

## Communication Protocols
- **Wi-Fi & HTTP**: Enables communication between hardware and the system.
- **Real-time Data Streaming**: Streams sensor data for immediate action.

## Contributors
- **Sinel Nemsara**
- **Thejan Rajapaksha**
- **Yohan Nanayakkara**
- **Sachitha Eshan**
- **Charith Bandara**
- **Devin Fernando**

## Conclusion
The DMS effectively integrates hardware and cloud technologies to monitor driver behavior, detect drowsiness, and improve road safety through real-time monitoring and data visualization.
