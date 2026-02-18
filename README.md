# STM32F411VET6 – Overview

## Introduction
The STM32F411VET6 is a 32-bit microcontroller from STMicroelectronics based on the ARM Cortex-M4 core.
It is designed for high-performance embedded applications and supports DSP and floating-point operations.

---

## Key Features
- ARM Cortex-M4 core with FPU
- Maximum Clock Frequency: 100 MHz
- 512 KB Flash Memory
- 128 KB SRAM
- Multiple GPIO Ports
- Timers (Advanced, General-purpose, Basic)
- 12-bit ADC
- USART, SPI, I2C, USB OTG FS
- DMA Controller
- Low-Power Modes

---

## Architecture
The STM32F411VET6 uses Harvard architecture with a 3-stage pipeline, enabling fast execution and efficient instruction handling.

---

## Pinout

Refer to the pinout diagram below:

![STM32F411 Pinout](https://github.com/user-attachments/assets/bcb766ee-6d64-48ed-9aaf-557b12a3e8de)

---

## Development Tools
- STM32CubeIDE
- STM32CubeMX
- HAL / LL Drivers
- ST-Link Programmer / Debugger

---

## Why STM32?
- High performance compared to 8-bit MCUs
- Rich peripheral support
- Strong ecosystem and documentation
- Widely used in industry

---

## Applications
- Motor Control
- IoT Systems
- Signal Processing
- Robotics
- Industrial Automation

---

## Author
**Jeffin Paul**

---

# 📁 PROJECTS

---

## 📡 UART – Bluetooth Control using STM32 and HC-05

This project demonstrates wireless LED control using STM32F411VET6 and HC-05 Bluetooth module.

Users can send `on` and `off` commands using a mobile app to control an LED.

### Components
- STM32F411VET6
- HC-05 Bluetooth Module
- LED + Resistor
- Android Phone

### Commands

| Command | Action |
|---------|---------|
| on      | LED ON  |
| off     | LED OFF |

---

## 🏠 Home Automation using STM32 and HC-05

A simple home automation system to control an LED wirelessly using Bluetooth.

### Commands

| Command | Action |
|---------|---------|
| 1       | LED ON  |
| 0       | LED OFF |

---

## 🌡️ Pressure and Temperature Monitoring using BMP280 (SPI)

This project reads temperature and pressure data from BMP280 sensor using SPI.

### Features
- SPI Communication
- Real-time Monitoring
- UART Output

### Voltage Warning
BMP280 works at **3.3V logic level**. Use a level shifter if required.

---

## 🔗 I2C Communication using STM32

Demonstrates I2C Master communication using STM32F411.

### I2C Pins

| STM32 Pin | Function |
|-----------|----------|
| PB8       | SCL      |
| PB9       | SDA      |

---

## 🚶 Smart Person Entry Monitoring System

A smart embedded system to count people entering using:

- LDR Sensor
- Laser Module
- OLED Display
- Buzzer

### Working Principle
1. Laser continuously shines on LDR
2. Beam interruption is detected
3. Counter increases
4. Buzzer beeps
5. OLED updates count

### Connections

#### OLED (I2C)

| OLED | STM32 |
|------|--------|
| VCC  | 3.3V   |
| GND  | GND    |
| SCL  | PB8    |
| SDA  | PB9    |

#### Laser

| Laser | STM32 |
|-------|--------|
| Signal| PB0    |

#### Buzzer

| Buzzer | STM32 |
|--------|--------|
| IN     | PB1    |

#### LDR

| LDR | STM32 |
|-----|--------|
| D0  | PA1    |

---

## 💻 Software Used
- STM32CubeIDE
- HAL Drivers
- Embedded C
- UART / SPI / I2C Protocols

---

## 📚 Additional Projects

- LED Blinking
- LED with Switch
- LDR Sensor
- Soil Moisture Sensor
- IR Sensor
- ADC
- ADC with Interrupt
- SysTick Timer
- Timers with Interrupt
- UART with Interrupt
- SPI Communication
- I2C Communication
- Bluetooth Control
- BMP280 Sensor

---

## 📜 License
This repository is open-source and free to use for educational purposes.
