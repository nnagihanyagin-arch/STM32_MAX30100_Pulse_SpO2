# STM32_MAX30100_Pulse_SpO2
PPG-based pulse rate and SpO₂ measurement system using STM32F401 and MAX30100 with OLED display and LED heartbeat indication.

STM32 MAX30100 Pulse and SpO₂ Measurement System
Abstract
This project presents a PPG-based pulse rate and oxygen saturation (SpO₂) measurement system implemented using an STM32F401 microcontroller and the MAX30100 biomedical sensor. The system acquires photoplethysmographic signals from the fingertip, processes the data in real time, and calculates heart rate and SpO₂ values. Each detected heartbeat is indicated by an LED, while the measured parameters are displayed on an SSD1306 OLED screen.
System Overview
The developed system consists of a MAX30100 optical sensor, an STM32F401 microcontroller, an SSD1306 OLED display, and an LED used for visual heartbeat feedback. Communication between the sensor, display, and microcontroller is established via the I2C protocol. The system is designed to operate in real time with low computational complexity and high measurement stability.
Measurement Principle
Pulse rate and SpO₂ measurements are based on photoplethysmography (PPG). Heart rate is calculated by detecting peaks in the infrared PPG signal. SpO₂ is estimated using the ratio-of-ratios method by analyzing the AC and DC components of red and infrared signals obtained from the MAX30100 sensor.
Hardware Components
STM32F401 Microcontroller
MAX30100 Pulse Oximeter Sensor
SSD1306 OLED Display
LED (heartbeat indication)
Breadboard and jumper wires
Software Structure
The firmware is developed using a modular approach and includes sensor drivers, signal processing algorithms, peak detection, SpO₂ estimation, and display control modules. Timer interrupts are used to ensure deterministic sampling and real-time operation.
Experimental Notes
During implementation, unstable I2C communication was observed due to missing or insufficient pull-up resistors on the MAX30100 module. External pull-up resistors were added on the I2C lines to ensure reliable data transmission.
Repository Structure
Core/ – STM32 firmware source and header files
Hardware/ – Circuit schematics and wiring diagrams
Photos/ – Real hardware implementation images
Docs/ – Project report
Reproducibility
All source codes, hardware schematics, and system photographs are provided in this repository to allow full reproduction of the proposed system.
Author
Nagihan
