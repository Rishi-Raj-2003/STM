# STM32F411VET6 – Introduction

## Overview
The STM32F411VET6 is a 32-bit microcontroller from STMicroelectronics based on the ARM Cortex-M4 core. It is designed for high-performance embedded applications and supports DSP and floating-point operations.

## Key Features
- ARM Cortex-M4 core with FPU
- Maximum clock frequency: 100 MHz
- 512 KB Flash memory
- 128 KB SRAM
- Multiple GPIO ports
- Timers (Advanced, General-purpose, Basic)
- ADC (12-bit)
- USART, SPI, I2C, USB OTG FS
- DMA controller
- Low-power modes

## Architecture
STM32F411VET6 uses a Harvard architecture with a 3-stage pipeline, enabling high-speed execution and efficient instruction handling.

## Pinout
Refer to the pinout diagram below:

<img width="1193" height="744" alt="image" src="https://github.com/user-attachments/assets/bcb766ee-6d64-48ed-9aaf-557b12a3e8de" />

## Development Tools
- STM32CubeIDE
- STM32CubeMX
- HAL / LL Drivers
- ST-Link (Programmer/Debugger)

## Why STM32?
- High performance compared to 8-bit MCUs
- Large peripheral set
- Strong ecosystem and documentation
- Industry adoption

## Applications
- Motor control
- IoT and connectivity projects
- Signal processing
- Robotics
- Industrial automation

# PROJECTS


## 📡 UART - Bluetooth Control using STM32 and HC-05

This project demonstrates wireless LED control using **STM32F411VET6** and the **HC-05 Bluetooth module** via UART communication.

By sending simple text commands (`on` / `off`) from a mobile phone using a Bluetooth serial app, an LED connected to the STM32 can be turned ON or OFF.

### 📸 Project Images

[<img width="692" height="1536" alt="image" src="https://github.com/user-attachments/assets/1deafa98-5ce0-4481-97fb-904bd466de73" />](https://chatgpt.com/backend-api/estuary/content?id=file_0000000038c072068e85d8cdb9522105&ts=491722&p=fs&cid=1&sig=a2c2f0cda3b284b978ad29dd3b1f4c431bf2d57bf6889643354fc5f1a486a1f0&v=0)

<img width="694" height="1536" alt="image" src="https://github.com/user-attachments/assets/24f418b1-cc2c-473e-843d-ce79be51ae78" />

### 🧩 Components Used

- STM32F411VET6 Development Board
- HC-05 Bluetooth Module
- LED
- Resistor (220Ω / 330Ω)
- Jumper Wires
- Android Mobile Phone

### 📱 Mobile Application Used

- **Serial Bluetooth Terminal** (Android App)

This app is used to send UART commands to the STM32 via Bluetooth.

### 🔌 Pin Connections

#### HC-05 Bluetooth Module

| HC-05 Pin | STM32 Pin | Description |
|-----------|-----------|-------------|
| VCC       | 3.3V / 5V | Power       |
| GND       | GND       | Ground      |
| TXD       | RX (PA10) | UART Receive|
| RXD       | TX (PA9)  | UART Transmit|

> ⚠️ Use a voltage divider for HC-05 RX if powered with 5V.

#### LED Connection

| LED Pin | STM32 Pin |
|---------|-----------|
| Anode   | GPIO Pin  |
| Cathode | GND       |

(With current-limiting resistor)

### ⚙️ Working Principle

1. The mobile phone connects to the HC-05 via Bluetooth.
2. The user sends commands using the mobile app.
3. HC-05 transmits data via UART.
4. STM32 receives the data through USART.
5. If the command is:
   - `on` → LED turns ON
   - `off` → LED turns OFF
6. The LED state changes accordingly.

### 💻 Software Used

- STM32CubeIDE
- STM32 HAL Drivers
- Embedded C
- UART Communication Protocol
- Serial Bluetooth Terminal App

### 📟 Commands

| Command | Action     |
|---------|------------|
| on      | LED ON     |
| off     | LED OFF    |

### ▶️ How to Run

1. Flash the program to STM32.
2. Power the board.
3. Pair HC-05 with mobile phone.
4. Open Serial Bluetooth Terminal app.
5. Connect to HC-05.
6. Send `on` or `off`.
7. Observe LED response.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🏠 Home Automation using STM32 and HC-05

This project demonstrates a simple **home automation system** using **STM32F411VET6** and the **HC-05 Bluetooth module**.

An LED is controlled wirelessly using a mobile phone via Bluetooth communication.


### 📸 Project Images

![WhatsApp Image 2026-02-09 at 3 06 14 PM](https://github.com/user-attachments/assets/f5495906-0cb2-491c-84c7-ace5ef989b2a)
![WhatsApp Image 2026-02-09 at 2 58 32 PM](https://github.com/user-attachments/assets/ce3833ba-ae07-4496-84fe-f1e4ae2d5874)

### 🧩 Components Used

- STM32F411VET6 Development Board
- HC-05 Bluetooth Module
- LED
- Resistor (220Ω / 330Ω)
- Jumper Wires
- Android Mobile Phone

### 📱 Mobile Application Used

- **Serial Bluetooth Terminal (Android App)**

Used to send control commands to the STM32.

### 🔌 Pin Connections

### HC-05 Bluetooth Module

| HC-05 Pin | STM32 Pin | Description |
|-----------|-----------|-------------|
| VCC       | 3.3V / 5V | Power       |
| GND       | GND       | Ground      |
| TXD       | RX (PA10) | UART RX     |
| RXD       | TX (PA9)  | UART TX     |

> ⚠️ Use a voltage divider for HC-05 RX when using 5V supply.

### LED Connection

| LED Pin | STM32 Pin |
|---------|-----------|
| Anode   | GPIO Pin  |
| Cathode | GND       |

(Use a current-limiting resistor.)

### ⚙️ Working Principle

1. The mobile phone connects to the HC-05 via Bluetooth.
2. The user sends commands from the mobile app.
3. HC-05 transmits data through UART.
4. STM32 receives the command.
5. Based on the received data:
   - `'1'` → LED turns ON
   - `'0'` → LED turns OFF
6. The LED responds instantly.

### 📟 Commands

| Command | Action   |
|---------|----------|
| 1       | LED ON   |
| 0       | LED OFF  |

### 💻 Software Used

- STM32CubeIDE
- STM32 HAL Drivers
- Embedded C
- UART Communication Protocol
- Serial Bluetooth Terminal App

### ▶️ How to Run

1. Flash the program to STM32.
2. Power the board.
3. Pair HC-05 with mobile phone.
4. Open Serial Bluetooth Terminal.
5. Connect to HC-05.
6. Send `1` or `0`.
7. Observe LED operation.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🌡️ Pressure and Temperature Monitoring using STM32 and BMP280 (SPI)

This project demonstrates real-time **pressure and temperature measurement**
using the **STM32F411VET6** microcontroller and the **BMP280 sensor** via **SPI communication**.

The sensor data is read and displayed through a serial terminal for monitoring and analysis.

### 📸 Project Images

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c3002d11-25cd-4d49-8c42-fffe193b091b" />

<img width="1522" height="749" alt="image" src="https://github.com/user-attachments/assets/5e6b0856-10d8-48f9-938c-a43906d89389" />

### 🧩 Components Used

- STM32F411VET6 Development Board
- BMP280 Pressure & Temperature Sensor
- Jumper Wires
- Breadboard (Optional)
- USB Power Supply
- Voltage Divider (if required)

### 🔌 Pin Connections (SPI Mode)

### BMP280 to STM32 (SPI)

| BMP280 Pin | STM32 Pin | Description |
|------------|-----------|-------------|
| VCC        | 3.3V      | Power       |
| GND        | GND       | Ground      |
| SCK        | SPI SCK   | Clock       |
| SDI (MOSI) | SPI MOSI  | Data In     |
| SDO (MISO) | SPI MISO  | Data Out    |
| CS         | GPIO / NSS| Chip Select |

> ⚠️ BMP280 works at **3.3V logic level**.  
> Use a voltage divider or level shifter if powering from 5V.

### ⚙️ Working Principle

1. STM32 communicates with BMP280 using SPI protocol.
2. Sensor continuously measures temperature and pressure.
3. STM32 reads raw sensor data.
4. Calibration formulas are applied.
5. Final values are calculated.
6. Results are transmitted to PC via UART.
7. User monitors values using a serial terminal.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🔗 I2C Communication using STM32

This project demonstrates **I2C (Inter-Integrated Circuit) communication**
using the **STM32F411VET6** microcontroller and external I2C devices.

It focuses on configuring the STM32 as an **I2C Master** and communicating
with peripheral modules such as sensors and displays.

### 📸 Project Images

<img width="452" height="755" alt="image" src="https://github.com/user-attachments/assets/e0edb617-fdcd-4bfd-9fb3-c55c278a0eb9" />
<img width="1916" height="1079" alt="image" src="https://github.com/user-attachments/assets/daaf24c4-68d2-410b-9e4a-90c01aa4412d" />

### 🧩 Components Used

- STM32F411VET6 Development Board
- I2C Module (Sensor / OLED / Peripheral)
- Jumper Wires
- Breadboard (Optional)
- USB Power Supply
  
### 🔌 Pin Connections (I2C)

### STM32 I2C1 Pins

| STM32 Pin | Function | Connected To |
|-----------|----------|--------------|
| PB8       | SCL      | I2C Clock    |
| PB9       | SDA      | I2C Data     |
| 3.3V      | VCC      | Module VCC   |
| GND       | GND      | Module GND   |

> ⚠️ Use pull-up resistors on SDA and SCL if the module does not have them onboard.

### ⚙️ Working Principle

1. STM32 is configured as I2C Master.
2. Peripheral device acts as I2C Slave.
3. Communication happens using SDA and SCL lines.
4. STM32 sends start condition and slave address.
5. Data is transmitted and received.
6. Stop condition ends communication.
7. Output is displayed via serial terminal or OLED.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Smart Person Entry Monitor using STM32

A smart embedded system to count people entering through a gate using
**STM32F411, LDR, Laser, OLED Display, and Buzzer**.

The system detects beam interruption and updates the count on an OLED screen
with buzzer alert.

### 📸 Project Setup

![WhatsApp Image 2026-02-18 at 2 54 35 PM](https://github.com/user-attachments/assets/81edfbb8-50ca-4e13-a275-4ccf7d493a65)


### 🧩 Components Used

- STM32F411 Development Board
- SSD1306 OLED Display (I2C)
- LDR Sensor Module
- Laser Module
- Active Buzzer
- Jumper Wires
- Breadboard (Optional)
- 3.3V Power Supply

### ⚙️ Working Principle

1. Laser continuously shines on the LDR sensor.
2. When a person blocks the beam, LDR output changes.
3. STM32 detects the interruption.
4. Counter is incremented.
5. Buzzer gives a beep.
6. OLED updates the count.

### 🔌 Pin Connections

### OLED (I2C)

| OLED | STM32 |
|------|--------|
| VCC  | 3.3V   |
| GND  | GND    |
| SCL  | PB8    |
| SDA  | PB9    |

### Laser

| Laser | STM32 |
|-------|--------|
| Signal| PB0    |
| VCC   | 3.3V   |
| GND   | GND    |

### Buzzer

| Buzzer | STM32 |
|--------|--------|
| IN     | PB1    |
| VCC    | 3.3V   |
| GND    | GND    |

### LDR

| LDR | STM32 |
|-----|--------|
| D0  | PA1    |
| VCC | 3.3V   |
| GND | GND    |


### 💻 Software Used

- STM32CubeIDE
- STM32 HAL Drivers
- Embedded C
- I2C Protocol

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Other Projects 

## LED Blinking
## LED with Switch
## LDR
## Soil Moisture Sensor
## IR Sensor
## ADC
## ADC with interrupt
## Systick timer
## Timer
## Timer with delay
## Timer with interrupt
## UART with Interrupt, UART with Bluetooth, UART_TX
## USART 1 , USART 6
## Turning on LED using Bluetooth communication
## SPI
## I2C
## Home Automation
## Checking pressure and temperature using BMP280
