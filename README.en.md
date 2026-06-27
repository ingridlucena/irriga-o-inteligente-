For the Portuguese version, click [here](README.md).  
For the English version, you are already here.

---

# Intelligent Monitoring and Automated Irrigation System 

This project consists of developing a prototype for an automated system to control, read sensors, and monitor a water reservoir and soil irrigation. The main objective is the practical application of automation, water efficiency, and low-level hardware manipulation concepts.

## System Operation
The system operates in a closed loop, continuously monitoring two main variables to make real-time control decisions:
* **Reservoir Monitoring:** The ultrasonic sensor measures the distance to the water level in centimeters. The algorithm processes this data to calculate and display the volumetric capacity of the reservoir (such as 75% or 100% of its maximum capacity) on the TFT screen.
* **Irrigation Control:** The capacitive soil moisture sensor constantly monitors how dry the soil is. When the moisture drops below the programmed critical threshold, the microcontroller triggers the relay module to turn on the water pump. As soon as the soil reaches ideal moisture, the system cuts the relay signal, stopping the irrigation to prevent water waste.
* **Environmental Data:** The DHT sensor performs secondary readings of ambient temperature and relative humidity for monitoring purposes on the display.

## Software Features
Unlike the conventional high-level scripts from the Arduino IDE, the software was developed by exploring the microcontroller's native architecture in pure C/C++:
* **Register Manipulation:** Manual and direct configuration of input and output ports through data direction registers (`DDRC` and `DDRD`) and direct state writing (`PORTD` and `PORTC`).
* **Classic Architecture:** Implementation using the `int main(void)` main function and a `while(1)` infinite control loop, optimizing execution flow and chip response time.

## Hardware Used
* **Microcontroller:** ATmega328P (Arduino Platform)
* **Visual Interface:** 1.8" TFT Screen (ST7735 Driver)
* **Sensors:** Capacitive Soil Moisture Sensor, Ultrasonic Sensor, and Ambient Temperature and Humidity Sensor (DHT)
* **Actuator:** Relay Module to trigger the water pump system

## Academic Context
Project developed as a practical activity for the Control and Automation Engineering course at UFRPE - UABJ, serving as a technical record and practical application report of programming and electronic circuit concepts.
