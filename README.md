# Interactive Sensor-Controlled Book

An interactive book built with Arduino. Sensors detect which page is
open and when the page is bent. The Arduino sends commands over serial
to a computer to play the matching video.

## How it works
- Two accelerometers (y-axis) are read on analog pins A2 and A3
- Value ranges identify the current page
  (for example 550-650 = page 1, 380-520 = page 3)
- A flex sensor (A0) above a threshold of 200 triggers video 4
- The Arduino sends serial commands ("video1", "video3", "play", ...)
  at 9600 baud
- State flags stop a video from retriggering over and over

## Hardware
- Arduino Uno R3
- 2 accelerometers
- 1 flex sensor

## Software
- Arduino C++ (book.ino), written in Arduino IDE 1.8.11
  
## Calibration and testing
- Printed live sensor values to the serial monitor to find the value
  range for each page
- Added short delays and flags to avoid repeated triggers

## What I learned
- Reading analog sensors with Arduino
- Calibrating thresholds from real measurements
- Debugging hardware and code together
## Demo
Video: [https://youtube.com/shorts/XKKZOa5GSXU?si=IhDM4um4DuJlzGsI]
