<img width="1280" alt="readme-banner" src="https://github.com/user-attachments/assets/35332e92-44cb-425b-9dff-27bcf1023c6c">

# [Project Name] 🎯
Touch-Me-Not Bot

## Basic Details
### Team Name: Mediocre Masters


### Team Members
- Team Lead: Amrita Reji - CET
- Member 2: Meera R S - CET
- Member 3: Vidya S R - CET

### Project Description
Our Touch-Me-Not Bot is pretty simple and straightforward. It is a poor bot that values it's personal space and doesn't like anyone(or anything for that matter!!) around it's proximity. It would blurt sligtly insulting dialogues when an object comes a bit close, and would scream heavy insults if anything comes too close to it.


### The Problem (that doesn't exist)
We didn't face any interesting problems..so we added a new problem to this world!The most useless problem the world needed!

### The Solution (that nobody asked for)
Oh wait...is our solution the problem? Oopsie:( 
What's more useless than a roast spitting bot! Our creative solution to a non-existent problem:))

## Technical Details
### Technologies/Components Used
For Software:
- Languages used- Arduino C++
- Frameworks used- Arduino IDE
- [Libraries used- Arduino core library- SD, SPI, TMRpcm
- [Tools used- Software tools:Arduino IDE,Serial Monitor, Library Manager
-              Hardware tools:Arduino UNO board, Soldering iron, Wire cutters, screwdrivers, breadboard and jumper wires, tape, LEDs, HC-SR04 ultrasonic sensor, SD card module, Speaker(3W), LM386 module

For Hardware:
- Arduino UNO board, Soldering iron, Wire cutters, screwdrivers, breadboard and jumper wires, tape, LEDs, HC-SR04 ultrasonic sensor, SD card module, Speaker(3W), LM386 module
Model: Arduino Uno
Sensor Type: Ultrasonic (e.g., HC-SR04) or Infrared Sensor
Detection Range:
Far: 15 - 40 cm
Medium: 5 - 15 cm
Close: < 5 cm

Audio Format: WAV
Storage: MicroSD card (4 GB)
Library: TMRpcm library for audio playback

LED Count: 3 LEDs for visual indication of distance categories (far, medium, close)

### Implementation
Hardware Assembly
The robot chassis was assembled accordingly. The components were connected as follows:

The HC-SR04 ultrasonic sensor was wired to the Arduino, with the VCC connected to 5V, GND to GND, Trig to pin 9, and Echo to pin 10.
The DFPlayer Mini was connected, with its VCC to 5V, GND to GND, TX to pin 11, and RX to pin 12. A small speaker was connected to the appropriate pins on the module.

The software was developed using the Arduino IDE. The necessary libraries for the DFPlayer Mini and ultrasonic sensor were installed. The code included functions for setting up the components, reading distance data, and playing audio clips. It was structured with a setup function for initialization and a loop function to continuously monitor distance and trigger insults.

Testing and Results
The robot was tested in various scenarios. It successfully detected objects within a distance of 40 cm and played random insults from pre-recorded audio files. Adjustments were made to the distance thresholds and motor speed based on testing results, enhancing its responsiveness.

Challenges and Solutions
During the project, several challenges were encountered, including wiring issues and bugs in the code that affected sensor readings. These were resolved by carefully checking connections and debugging the code step-by-step, leading to successful functionality.

# Installation
same thing

# Run
[commands]

### Project Documentation

1. Project Overview
Project Name:Touch me not
Objective: To create a robot that does absolutely nothing meaningful except deliver unwanted, randomly timed verbal jabs to anyone within range. Because why not?
Features:
Spits out random mild insults whenever it senses someone, ensuring it is almost never silent.
Flashes some LEDs to keep itself looking vaguely busy.
Designed to feel essential but contribute zero real value.
2. Project Requirements
Hardware Components:
Microcontroller: Necessary, apparently, to make the magic happen. But does it really?
Ultrasonic Sensor: Needed to detect when someone’s nearby, purely for initiating sarcastic remarks.
SD Card Module: Solely holds insult audio files. Quite a one-trick pony.
Speaker: So the robot can broadcast these files to everyone’s delight…or annoyance.
LM386 amplifier module:For amplifying audio.
Software and Libraries:
Arduino IDE: Minimal coding efforts for minimal output.
Libraries like TMRpcm (because an insult with no sound is no insult at all) and SD (to ensure insults are never in short supply).
4. System Specifications
Microcontroller Specs: Standard enough to carry out minimal tasks without breaking a sweat.
Sensor Range and Accuracy: Just precise enough to detect anyone unlucky enough to be in the area.
Audio Playback: Loud enough to make its pointless statements clearly audible.
Power Specifications: Lasts long enough to ensure the insults keep coming.
Physical Design: Small and easily concealable, for maximum accidental encounters.

# Screenshots (Add at least 3)
![Work1](https://github.com/user-attachments/assets/1a285be3-876d-444e-bdb6-11991d9509cc)
This is a picture of the arduino board during one of the initial connection stages. Here the LEDs, sensor and speaker are connected amd the code for the speakers to play audio is being verified, while the other member extracts the necessary audio files.


![sensortest](https://github.com/user-attachments/assets/a82411d4-03b1-46fb-997b-4846f251111d)
This picture shows us testing the sensor and audio files by placing the hands at different distances as specified.


![finalsetup](https://github.com/user-attachments/assets/9a25e45b-a04f-4853-b4a5-5b34bf8fd6be)
This is a picture of the final setup of our product with all the componenets attached!

# Diagrams
![Workflow](Add your workflow/architecture diagram here)
*Add caption explaining your workflow*

For Hardware:

# Schematic & Circuit
![Circuit](https://github.com/user-attachments/assets/c242f1e8-bcfa-4ec9-8a18-5015cb80e1f6)


![Schematic](Add your schematic diagram here)
*Add caption explaining the schematic*

# Build Photos

![finalsetup](https://github.com/user-attachments/assets/9a25e45b-a04f-4853-b4a5-5b34bf8fd6be)
Components:Hardware tools:Arduino UNO board, Soldering iron, Wire cutters, screwdrivers, breadboard and jumper wires, tape, LEDs, HC-SR04 ultrasonic sensor, SD card module, Speaker(3W), LM386 module

![build1](https://github.com/user-attachments/assets/e45f24df-54ed-41fc-8b63-4d9e11c1079e)
![sensortest](https://github.com/user-attachments/assets/ef56d8cf-37ae-42d0-b03e-8df0b4db07c2)
![Work1](https://github.com/user-attachments/assets/95773f90-9cd2-4b31-ab4b-4295e6da9788)
Hardware Assembly
The robot chassis was assembled accordingly. The components were connected as follows:

The HC-SR04 ultrasonic sensor was wired to the Arduino, with the VCC connected to 5V, GND to GND, Trig to pin 9, and Echo to pin 10.
The DFPlayer Mini was connected, with its VCC to 5V, GND to GND, TX to pin 11, and RX to pin 12. A small speaker was connected to the appropriate pins on the module.

The software was developed using the Arduino IDE. The necessary libraries for the DFPlayer Mini and ultrasonic sensor were installed. The code included functions for setting up the components, reading distance data, and playing audio clips. It was structured with a setup function for initialization and a loop function to continuously monitor distance and trigger insults.

Testing and Results
The robot was tested in various scenarios. It successfully detected objects within a distance of 40 cm and played random insults from pre-recorded audio files. Adjustments were made to the distance thresholds and motor speed based on testing results, enhancing its responsiveness.

Challenges and Solutions
During the project, several challenges were encountered, including wiring issues and bugs in the code that affected sensor readings. These were resolved by carefully checking connections and debugging the code step-by-step, leading to successful functionality.



![finalsetup](https://github.com/user-attachments/assets/6a3d22cf-fb71-42ea-8c70-17ca431cab73)


### Project Demo
# Video
[Add your demo video link here]
*Explain what the video demonstrates*

# Additional Demos
[Add any extra demo materials/links]

## Team Contributions
- Amrita Reji: Connected the circuit and debugging of code
- Meera R S: Coding and testing 
- Vidya S R: Coding, testing and audio editing

---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProject--24-24?link=https%3A%2F%2Fwww.tinkerhub.org%2Fevents%2FQ2Q1TQKX6Q%2FUseless%2520Projects)



