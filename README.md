# Temperature and Humidity Sensing System with STM32 RT-Spark

This project implements a real-time temperature and humidity sensing system using the **RT-Thread RT-Spark development board**, the **AHT21 sensor**, and a **240×240 ST7789 LCD**. It reads environmental data via I²C and displays it on the LCD using embedded C code written in **STM32CubeIDE**.

## 📦 Features

- Real-time temperature and humidity monitoring
- LCD display output using FSMC parallel interface
- Embedded C implementation using STM32 HAL drivers
- Modular code structure for easy reuse and adaptation

## 🧰 Hardware Requirements

| Component | Description |
|----------|-------------|
| RT-Spark Development Board | STM32F407ZGTx-based board with RT-Thread RTOS |
| AHT21 Sensor | I²C digital temperature and humidity sensor (ADDR: 0x38) |
| ST7789 LCD | 1.3" 240×240 display, FSMC parallel interface |
| ST-Link Programmer | For flashing and debugging |
| USB Cable | Power and programming |

## 💻 Software Requirements

- STM32CubeIDE
- STM32 HAL Libraries
- AHT21 driver (included)
- ST7789 LCD driver (included)

## 📁 Repository Structure
├── main.c               # Main application logic ├── drv_aht21.c/h        # AHT21 sensor driver ├── drv_lcd.c/h          # ST7789 LCD driver ├── drv_lcd_font.h       # Font definitions for LCD text rendering ├── CubeIDE/.ioc         # STM32CubeIDE configuration fil


## ⚙️ Setup Instructions

1. Open STM32CubeIDE and import the project.
2. Ensure `.ioc` file is configured with:
   - **I²C1 enabled** (PF0 = SCL, PF1 = SDA)
   - **FSMC enabled** for LCD parallel interface
3. Connect AHT21 sensor and LCD to the RT-Spark board as per schematic.
4. Build and flash the firmware using ST-Link.
5. Observe temperature and humidity readings on the LCD.

## 📷 Output Example
RT-Spark AMT21 Temp: 30.91°C Hum: 71.18% Sensor: AMT21


## 🧪 Lab Context

This project was developed as part of **Laboratory Activity No. 4** for BCA152 Microcontrollers at **Mindanao State University – Iligan Institute of Technology**.

## 🙌 Credits

Developed by Angeli MVU04  
Instructor: Paul Rodolf P. Castor, MSCA  
Platform: RT-Thread RT-Spark STM32 Board
