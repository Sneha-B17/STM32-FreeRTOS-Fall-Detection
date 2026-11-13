# STM32 FreeRTOS-Based Fall Detection System

## 📌 Project Overview

This project implements a real-time fall detection system using the STM32F429ZIT6 microcontroller, FreeRTOS and the MPU6050 motion sensor.

The system continuously monitors acceleration and orientation data to detect potential fall events. FreeRTOS is used to divide the application into multiple independent tasks, improving modularity and real-time execution.

The detected fall status is displayed on a 16×2 LCD and transmitted to a PC through UART communication using Tera Term.

## 🛠️ Hardware and Software Requirements

**Hardware**
- STM32F429ZIT6 Discovery Board
- MPU6050 Accelerometer and Gyroscope
- 16×2 LCD Display
- USB-to-Serial / UART monitoring setup

**Software**
- Embedded C
- STM32CubeIDE
- FreeRTOS
- Tera Term

## ⚙️ Features

- Real-time motion monitoring using MPU6050.
- Acceleration-based fall detection.
- Orientation and tilt monitoring.
- Multitasking using FreeRTOS.
- Sensor interfacing through I2C3.
- Fall status displayed on a 16×2 LCD.
- Sensor readings and fall alerts displayed on Tera Term through UART.

## 🏗️ FreeRTOS Task Architecture

The application is divided into three main tasks:

### 1. Watcher Task
- Monitors motion sensor readings.
- Collects acceleration data from MPU6050.

### 2. Thinker Task
- Processes sensor readings.
- Evaluates acceleration and tilt conditions.
- Determines potential fall events.

### 3. Shouter Task
- Handles fall detection alerts.
- Updates the LCD display.
- Reports detection status through UART.

## 📡 Sensor Interfacing

The MPU6050 sensor communicates with the STM32F429ZIT6 through I2C3.

- I2C communication is used to read accelerometer and gyroscope data.
- Accelerometer readings are used to calculate motion magnitude.
- Orientation information is used to evaluate tilt conditions.

## 📟 Output Interfaces

**16×2 LCD Display**

Displays the fall detection status directly on the embedded hardware.

**Tera Term**

Displays sensor readings and fall detection messages through UART serial communication.

## 📚 Concepts Learned

- Real-Time Operating Systems (RTOS).
- FreeRTOS task creation and scheduling.
- Multitasking and task coordination.
- MPU6050 sensor interfacing.
- I2C and UART communication.
- Accelerometer data processing.
- Real-time event detection.
- Embedded C programming.

## 🔮 Future Enhancements

- Add wireless emergency notifications.
- Improve fall detection accuracy.
- Implement additional sensor fusion techniques.
- Add data logging and event history.

## 👩‍💻 Author

**Sneha B.**

Embedded C | STM32 | FreeRTOS | RTOS | Embedded Systems
