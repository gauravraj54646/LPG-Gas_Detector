# LPG-Gas_Detector# Fire Sensor Alarm Project

This repository contains the code and resources for a Fire Sensor Alarm project that utilizes a flame sensor and Arduino to detect potential fire incidents and trigger an alarm.

## Table of Contents

- [Introduction](#introduction)
- [Demo](#demo)
- [Circuit Diagram](#circuit-diagram)
- [Simulation](#simulation)
- [Setup Instructions](#setup-instructions)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Fire Sensor Alarm project is designed to detect the presence of flames and unusual temperature changes, indicating a potential fire hazard. When a flame or significant temperature increase is detected, the system activates an alarm to promptly alert users about the potential danger.

## Components List

| Name   | Quantity | Component                |
|--------|----------|--------------------------|
| U1     | 1        | Arduino Uno R3           |
| PIEZO1 | 1        | Piezo                    |
| D1     | 1        | Red LED                  |
| D2     | 1        | Green LED                |
| R1, R2 | 2        | 1 kΩ Resistor            |
| U2     | 1        | Temperature Sensor [TMP36]/Flame Sensor|


## Demo

[Video upload pending]

## Circuit Diagram

![Circuit Diagram](https://github.com/adityakanu/Fire-Alarm-Sensor/blob/0805cbb021270aadbb464f752a95485cd2f7fbc1/Fire%20alarm%20sensor.png)

Also look upon: [Schematic View](https://github.com/adityakanu/Fire-Alarm-Sensor/blob/0805cbb021270aadbb464f752a95485cd2f7fbc1/Fire%20Sensing%20Alarm.pdf)

## Circuit Description:

1. The flame sensor (PIEZO1) is connected to one of the analog input pins of the Arduino Uno (A0, for example). The analog voltage output from the flame sensor is read by the Arduino to detect the presence of a flame.

2. The red LED (D1) is connected to a digital output pin of the Arduino (such as D3). When the flame sensor detects a flame, the Arduino sends a signal to illuminate the red LED, indicating that the fire alarm has been triggered.

3. The green LED (D2) is connected to another digital output pin of the Arduino (e.g., D4). The green LED remains on under normal conditions. When the alarm is triggered, the Arduino turns off the green LED.

4. The 1 kΩ resistors (R1, R2) are connected in series with the LEDs to limit the current passing through them and prevent excessive current flow.

5. The temperature sensor (U2) is used to monitor the ambient temperature. The Arduino can analyze temperature changes in conjunction with flame sensor data to enhance the accuracy of fire detection.

This circuit is designed to provide a basic fire-sensing alarm system using a flame sensor and Arduino. When the flame sensor detects a flame, the red LED lights up, and the green LED turns off, alerting users to the potential presence of a fire.

Overall System Functionality:
 - The flame sensor serves as the primary input to the system, detecting the presence of a flame or fire.
 - The Arduino processes the flame sensor's signal and determines whether a fire hazard is present.
 - The system responds by illuminating the red LED to provide a visual fire alarm indicator and activating the piezo buzzer to sound an audible alarm, effectively notifying users of the potential fire threat.

## Simulation

You can simulate the Fire Sensor Alarm project using [Tinkercad](https://www.tinkercad.com/). Click [here](https://www.tinkercad.com/things/1iVVr0knjMJ) to access the simulation.

1. Start the simulation
2. Increase the temperature of the temperature sensor.

Note: We have used only the temperature sensor as the Flame Sensor module is not available on Tinkercad. But the Flame Sensor is shown in the [demo](#demo).

## Setup Instructions

Follow these steps to set up and run the Fire Sensor Alarm project:

1. Hardware Connections and Initial Setup:
   - Connect the flame sensor (U2) to a digital pin (e.g., D2) on the Arduino (U1).
   - Connect the red LED (D1) to a digital pin (e.g., D3) on the Arduino and the green LED (D2) to another digital pin (e.g., D4).
   - Attach the piezo buzzer (PIEZO1) to a digital pin (e.g., D5) on the Arduino.
   - Power the Arduino using a USB cable or an appropriate power source.

2. Software Installation and Code Uploading:
   - Install the Arduino IDE on your computer if not already installed.
   - Connect the Arduino to your computer via USB and open the Arduino IDE.
   - Download and load the code for the Fire Sensor Alarm project onto the Arduino.
   - Ensure that you have the necessary libraries installed for working with digital inputs/outputs and controlling the piezo buzzer.

3. Configuration Settings and Parameters:
   - Open the Arduino code in the IDE and review the code comments to understand its functionality and logic.
   - Depending on the flame sensor used, there may be a need to adjust threshold values for flame detection. These values can be modified within the code to fine-tune the sensitivity.
   - If desired, you can modify the pins assigned for the LEDs and piezo buzzer to match your hardware connections.

4. Interpreting Alarm Signals and Response:
   - When the flame sensor detects a flame, it sends a HIGH signal to the Arduino.
   - The Arduino, upon receiving the flame detection signal, activates the red LED to indicate a fire alarm.
   - Additionally, the piezo buzzer is activated, producing an audible alarm sound to alert users of a potential fire hazard.
   - The green LED remains off under normal conditions.
   - In response to the alarm, users should take appropriate actions based on their safety protocols, such as evacuating the area, notifying authorities, or addressing the source of the flame.

5. Testing and Monitoring:
   - Test the Fire Sensor Alarm project by introducing a controlled flame source near the flame sensor.
   - Observe the behaviour of the LEDs and the piezo buzzer when a flame is detected.
   - Monitor the system's responsiveness and accuracy in detecting flame incidents.
   - Regularly check and maintain the system to ensure its proper functioning and reliability.

By following these steps, you can set up, operate, and monitor the Fire Sensor Alarm project. This project serves as an early warning system, providing visual and audible alerts to help detect and respond to potential fire incidents promptly.

## Contributing

Contributions are welcome! If you'd like to contribute to the project via documentation or circuit design improvements, please follow these steps:

1. Fork the repository.

2. Create a new branch for your feature or bug fix: `git checkout -b feature-name`.

3. Make your changes and commit them: `git commit -m 'Description of your changes'`.

4. Push to the branch: `git push origin feature-name`.

5. Open a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
