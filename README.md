# Smart Door — Arduino Embedded System with WiFi Control

An automated smart door system combining ultrasonic proximity sensing, servo-driven door control, an LCD status display, and remote WiFi control via an ESP8266 module.

## Features
- **Automatic mode:** an ultrasonic sensor (HC-SR04) detects proximity and opens the door automatically when someone approaches within a set threshold
- **Auto-close:** the door closes automatically after a set delay once opened
- **Status feedback:** LCD screen displays current mode (Auto/Manual) and door state (Open/Closed); LED indicators (red = closed, green = open) and a buzzer confirm actions
- **Remote WiFi control:** the ESP8266 module connects to a WiFi network and runs a lightweight server, communicating over AT commands via `SoftwareSerial`, allowing the door to be controlled remotely
- **Auto/Manual mode toggle**

## Hardware Components
- Arduino board
- ESP8266 WiFi module
- HC-SR04 Ultrasonic Sensor
- Servo Motor (door mechanism)
- 16x2 LCD Display
- Red & Green LEDs
- Buzzer

## Tech Stack
- C/C++ (Arduino framework)
- ESP8266 AT command set (via `SoftwareSerial`)
- `Servo` and `LiquidCrystal` libraries

## How to Run
1. Wire the components as described in `hardware connections of the project.pdf` (full pin-by-pin wiring guide)
2. Open `final_project.ino` in the Arduino IDE
3. **Set your own WiFi credentials** in the `ssid` and `password` variables at the top of the file
4. Upload the sketch to your Arduino
5. Open the Serial Monitor (9600 baud) to see connection status and the assigned IP address

## Security Note
WiFi credentials in this repository are redacted. Never commit real WiFi credentials to a public repository — always set your own locally before uploading to your board.
