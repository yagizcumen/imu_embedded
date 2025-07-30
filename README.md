# imu_embedded

# ATmega328P AU with VL53L0X (mmcu5603nj) and LSM6DSM Integration

This project demonstrates the integration of the **ATmega328P AU** microcontroller with a **VL53L0X-based mmcu5603nj Time-of-Flight sensor** and an **LSM6DSM 6-axis IMU module**, creating a compact and efficient inertial measurement system. The ATmega328P AU is responsible for I2C communication with both sensors, collecting real-time distance and motion data for robotics, automation, and navigation tasks.

This repository contains all the necessary firmware, schematics, and documentation to help you set up and adapt the system to your needs.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Hardware Components](#hardware-components)
- [License](#license)

---

## Project Overview

![imuduino3](https://github.com/user-attachments/assets/7957ec79-ee7a-43f8-bd64-bf6ad8ec6920)  
![imuduino2](https://github.com/user-attachments/assets/ce3af49e-50b6-4142-89d8-3ff834f750c3)

This embedded system uses the **ATmega328P AU** microcontroller to coordinate two key sensors:

- **mmcu5603nj**: a compact **VL53L0X Time-of-Flight (ToF)** sensor for accurate short-range distance measurement.
- **ls6dsm**: an **LSM6DSM 6-axis IMU**, combining accelerometer and gyroscope functionality for motion tracking.

Together, they allow for real-time detection of both spatial proximity and motion orientation, useful in a variety of applications such as SLAM, obstacle avoidance, or wearable device development.

---

## Hardware Components

### 1. ATmega328P AU

The **ATmega328P AU** is a popular 8-bit AVR microcontroller, well known from Arduino Uno boards (SMD version). In this project, it serves as the central controller and communicates with both sensors over I2C.

- 32 KB Flash, 1 KB SRAM
- I2C, SPI, UART interfaces
- 23 digital I/O pins
- 6-channel 10-bit ADC
- Used for data collection, processing, and serial output of sensor data

---

### 2. mmcu5603nj — VL53L0X ToF Sensor

The **mmcu5603nj** module is based on the **VL53L0X**, a Time-of-Flight laser-ranging sensor from STMicroelectronics.

- Range: ~30mm to 2 meters
- Resolution: millimeter-level precision
- Communication: I2C (Address configurable)
- Fast response time for real-time obstacle detection
- Low-power and compact form factor

Used for proximity sensing in robots, gesture-based UI systems, and short-range LIDAR-like applications.

---

### 3. ls6dsm — LSM6DSM 6-axis IMU

The **ls6dsm** is a sensor module built around the **LSM6DSM**, which integrates:

- 3-axis Accelerometer
- 3-axis Gyroscope
- Communication: I2C or SPI
- Output Data Rates (ODR): up to 6.6 kHz
- High precision motion detection

Commonly used in robotics, mobile devices, drones, and wearables for orientation tracking, fall detection, and step counting.

---

## License

This project is open-source and distributed under the [MIT License](LICENSE).
