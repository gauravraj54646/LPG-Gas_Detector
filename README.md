# LPG-Gas_Detector

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
| PIEZO1 | 1        | Piezo Burzer             |
| D1     | 1        | Red LED                  |
| D2     | 1        | Green LED                |
| R1, R2 | 2        | 1 kΩ Resistor            |
| Exhaust Fan | 2   | 5v , 1.8 watt            |
| R1, R2 | 2        | 1 kΩ Resistor            |
| U2     | 1        | MQ6 Gas Sensor           |


## Demo

[Video upload pending]

## Circuit Diagram

![Circuit Diagram](https://github.com/adityakanu/Fire-Alarm-Sensor/blob/0805cbb021270aadbb464f752a95485cd2f7fbc1/Fire%20alarm%20sensor.png)

Also look upon: [Schematic View](https://github.com/adityakanu/Fire-Alarm-Sensor/blob/0805cbb021270aadbb464f752a95485cd2f7fbc1/Fire%20Sensing%20Alarm.pdf)

Circuit Connection Steps:

1. Power Supply to Arduino

Connect the 9V battery's positive terminal to the Vin pin of the Arduino.

Connect the negative terminal to the GND pin of the Arduino.



2. Gas Sensor (MQ-2)

VCC of the gas sensor to 5V on Arduino.

GND of the gas sensor to GND on Arduino.

Digital output (DO) of the gas sensor to pin 8 on Arduino.



3. Buzzer

Positive terminal of the buzzer to pin 8 on Arduino.

Negative terminal of the buzzer to GND.



4. Fan Control

Connect the positive terminal of the fan to the NO (Normally Open) pin of the relay module.

Connect the negative terminal of the fan to the negative terminal of the 9V battery.

Connect the positive terminal of the 9V battery to the COM (Common) pin of the relay module.



5. Relay Module

VCC of the relay to 5V on Arduino.

GND of the relay to GND on Arduino.

IN pin of the relay to pin 9 on Arduino.



6. Motor Control

Connect the motor's positive terminal to the relay's NO pin.

Connect the motor's negative terminal to the negative terminal of another 9V battery.

Connect the positive terminal of the second 9V battery to the COM pin of the relay.



7. Switch

Connect the switch to break the positive line between the 9V battery and the Arduino for manual control.




These steps correspond to the provided diagram. Let me know if you need additional clarification!

## Circuit Description:
Overall System Functionality:

1. Input Detection (Gas Sensor - MQ-2):

The gas sensor continuously monitors the environment for gas leakage.

If the gas concentration exceeds the set threshold, it sends a HIGH signal to Arduino through Digital Output (DO).



2. Alarm Activation (Buzzer):

When the gas sensor detects leakage, Arduino triggers the buzzer connected to pin 8.

The buzzer produces a sound to alert users about the gas leak.



3. Ventilation System (Fan Control via Relay):

Arduino activates the relay module connected to pin 9, which powers the fan.

The fan helps in ventilating the area by removing leaked gas.



4. Safety Shutdown (Motor Control via Relay):

The motor (valve control) can be used to shut off the gas supply by closing the valve if leakage is detected.

Arduino triggers this action through the relay module connected to the motor.



5. Manual Control (Switch):

A manual switch allows users to disconnect power to the system for maintenance or emergency shutdown.



6. Power Supply:

The system operates using 9V batteries for both the Arduino and external devices like the motor and fan.




Final Purpose:

This system is designed for gas leakage detection and safety management by activating alarms, improving ventilation, and optionally shutting off gas flow, ensuring safety in residential or industrial environments.


Overall System Functionality:
This project detects LPG gas leaks and ensures safety by activating necessary countermeasures.
• The MQ6 sensor detects LPG or its composition in the air, triggering a buzzer for alerting.
• Automatically cuts off the house’s electric connection and starts the exhaust fan to remove the leaked gas.
• Sensors/instruments/tools: MQ6 sensor, buzzer, relay module, exhaust fan, Arduino .
## Simulation

You can simulate the Fire Sensor Alarm project using [Tinkercad](https://www.tinkercad.com/). Click [here](https://www.tinkercad.com/things/1iVVr0knjMJ) to access the simulation.

1. Start the simulation
2. Increase the temperature of the temperature sensor.

Note: We have used only the temperature sensor as the Flame Sensor module is not available on Tinkercad. But the Flame Sensor is shown in the [demo](#demo).




## Contributing

Contributions are welcome! If you'd like to contribute to the project via documentation or circuit design improvements, please follow these steps:

1. Fork the repository.

2. Create a new branch for your feature or bug fix: `git checkout -b feature-name`.

3. Make your changes and commit them: `git commit -m 'Description of your changes'`.

4. Push to the branch: `git push origin feature-name`.

5. Open a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
