# SmartLight

## Overview
SmartLight is a light control system that grants wireless manipulation over 12V LED stripe.

## Description
The heart of the project is a STM32F4DISCOVERY board managing the whole system.
It contains bluetooth module for wireless comunication, analog ambient light sensor and motion detector.
Application software is written in **C** using *HAL* library.

SmartLight supported wireless operations:
 - Switching light on and off,
 - Switching light on and off due to motion detection,
 - Adjusting light intensity based on the intensity of ambient light,
 - Manually modifying light intensity (20% intervals).

## Tools

Hardware:
 - STM32F4DISCOVERY (STM32F407VG),
 - HC-06 FC-114 Bluetooth module,
 - PIR HC-SR501 Motion detector,
 - DFRobot Gravity PT550 Analog ambient light sensor,
 - Self made relay module using N-MOSFET transistor.
 
Software:
 - STM32CubeMX,
 - System Workbench for STM32,
 - STMStudio,
 - Serial Bluetooth Terminal application for Android.

## How to run

 - Open project in System Workbench for STM32,
 - Connect external devices to the STM32,
 - Build and run.
 
 #### Pinout
 
|  | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| A |  | Ambient light sensor |
| B |
| C |  |  |  |  |  |  |  |  |  |  | Bluetooth TxD | Bluetooth RxD |  |  | Motion Detector |
| D |  |  |  |  |  |  |  |  |  |  |  |  |  Transistor Gate|


#### How to use

 - Install bluetooth terminal application on Your smartphone (we recommend using 'Serial Bluetooth Terminal' for Android),
 - Connect to the bluetooth module,
 - Control the light using codes given below.
 
 #### Codes
 
| | | 
|--|--|
| 'O' | Switch the light ON|
| 'F' | Switch the light OFF|
| 'M' | Motion detection ON|
| 'A' | Ambient light intensity sensor ON|
| 'B' | Motion detection and ambient light intensity sensor ON|
| '0' | Set light intensity to 0%|
| '2' | Set light intensity to 20%|
| '4' | Set light intensity to 40%|
| '6' | Set light intensity to 60%|
| '8' | Set light intensity to 80%|
| '1' | Set light intensity to 100%|

## Future improvements

 - Controlling high voltage light sources,
 - Wireless connection using WiFi.
 
 ## License
 MIT (see LICENSE.md)
 
 ## Credits
 Authors:
 
 - Łukasz Kowalik
 - Mateusz Durlak
 - Hubert Jankowski

 The project was conducted during the Microprocessor Lab course held by the
Institute of Control and Information Engineering, Poznan University of Technology.
Supervisor: Adam Bondyra
