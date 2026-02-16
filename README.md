# Home-Automation-System-Using-IoT-with-ESP32-CAM
Project Description: IoT-Based Home Automation System with ESP32-CAM and MIT App Inventor
Overview
This project is an advanced IoT-based home automation system that leverages the ESP32-CAM module, Firebase for real-time database management, and a custom mobile application built using MIT App Inventor. The system allows users to remotely control home appliances, monitor real-time camera feeds, and enhance home security with motion detection and keypad access.

Components
ESP32-CAM: A microcontroller with an integrated camera module used for streaming video, capturing images, and integrating with the home automation system.
PCF8575 I/O Expander: Extends the GPIO capabilities of the ESP32-CAM for controlling multiple relays.
Firebase: Real-time database for managing the state of appliances and storing camera data.
MIT App Inventor: A visual programming environment used to build the mobile app for user interaction with the system.
Keypad and LCD: Used for secure entry with a password-protected system and for displaying messages.
Relays: For switching home appliances on and off.
PIR Motion Sensor: Detects motion for security purposes.
Features
Remote Control of Appliances:

Users can turn on/off appliances via the mobile app.
Six relays control different home appliances.
Real-Time Camera Feed:

The ESP32-CAM streams live video which can be accessed through the mobile app.
Supports capturing images on-demand.
Security Features:

Motion detection using a PIR sensor. When motion is detected, an alert can be sent to the user, and the camera can capture an image.
Password-protected entry using a keypad. The system checks the entered password against predefined passwords and grants or denies access accordingly.
Real-Time Updates:

The system uses Firebase to keep the state of the appliances updated in real-time.
Any changes made via the mobile app are immediately reflected in the system.
System Architecture
ESP32-CAM Initialization:

Initializes WiFi and connects to Firebase.
Configures the camera settings and starts the camera server.
Sets up GPIO pins for relays, motion sensor, and keypad.
Mobile App (MIT App Inventor):

The app allows users to control the relays, view the camera feed, and receive alerts.
Communicates with Firebase to send and receive data.
Firebase Integration:

Real-time database stores the state of each relay.
Streams data to the ESP32-CAM to update relay states based on user commands.
User Authentication:

Keypad input is processed and compared with predefined passwords.
Correct password input unlocks the system, while incorrect input triggers an alert.
Implementation Details
ESP32-CAM Setup:

Configures the camera, initializes WiFi, and connects to Firebase.
Starts the HTTP server for camera streaming.
Relay Control:

PCF8575 I/O expander is used to control six relays.
Relays are toggled based on commands received from Firebase.
Motion Detection:

PIR sensor is set up to detect motion and trigger alerts.
When motion is detected, an image is captured and stored.
Keypad Security:

4x4 matrix keypad is used for password entry.
LCD displays messages based on the status of the input (correct/incorrect).
Firebase Integration:

The system streams data to and from Firebase to ensure real-time updates.
Callback functions handle changes in the database and update the system accordingly.
Mobile App (MIT App Inventor) Functionality
User Interface:

Buttons to control each relay.
Video feed display from the ESP32-CAM.
Notifications for motion detection and system status.
Firebase Communication:

The app reads and writes data to Firebase to control the system.
Real-time synchronization ensures that the app and the system are always in sync.
Conclusion
This IoT-based home automation system provides a robust and flexible solution for remote home control and monitoring. By integrating the ESP32-CAM with Firebase and a custom-built mobile app, users can enhance their home security, convenience, and efficiency. The system's real-time capabilities and security features make it a valuable addition to any smart home setup.
