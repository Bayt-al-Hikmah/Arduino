# Arduino Fundamentals 

This course provides a structured introduction to Arduino programming, and microcontroller development. It is designed for beginners who want to understand both the theoretical foundations of electronics and the practical use of Arduino for embedded systems projects.

The course is divided into 5 lectures, progressing from basic electrical concepts to low-level microcontroller programming.

![Lectures](https://img.shields.io/badge/Lectures-5-00c896?style=flat-square)
![Board](https://img.shields.io/badge/Board-Arduino%20UNO-ff6b35?style=flat-square)
![MCU](https://img.shields.io/badge/MCU-ATmega328P-4a9eff?style=flat-square)
![Language](https://img.shields.io/badge/Language-C%20%2F%20C%2B%2B-c77dff?style=flat-square)
![Level](https://img.shields.io/badge/Level-Beginner%20→%20Advanced-ffd166?style=flat-square)



## 📋 Table of Contents

- [Course Overview](#-course-overview)
- [Curriculum](#-curriculum)
  - [Lecture 1 Foundations](#lecture-1--foundations--electricity-electronics--microcontrollers)
  - [Lecture 2 Arduino Basics](#lecture-2--arduino-platform--setup-ide--programming-basics)
  - [Lecture 3 GPIO & Motors](#lecture-3--gpio-sensors-actuators--motors)
  - [Lecture 4 Displays & Communication](#lecture-4--displays-communication-protocols--wireless)
  - [Lecture 5 Low-Level Programming](#lecture-5--atmega328p-low-level-programming--register-configuration)
- [Prerequisites](#-prerequisites)
- [Learning Path](#-learning-path)


## Course Overview

| | |
|---|---|
| 📚 **Lectures** | 5 structured modules |
| 🔌 **Hardware** | Arduino UNO (ATmega328P) |
| 💻 **IDE** | Arduino IDE 2.x |
| 🎯 **Level** | Absolute beginner → Low-level embedded |
| ⚙️ **Language** | C / C++ (Arduino framework + bare AVR-C) |
| 📡 **Protocols** | UART · SPI · I²C · Bluetooth · Wi-Fi |


## Curriculum

### Lecture 1 Foundations: Electricity, Electronics & Microcontrollers

This lecture begins where all electronics begin with static electricity and the nature of electric charge, then progressively builds toward the components and concepts needed to understand embedded systems.

**Topics covered:**

- Static electricity, electric charge, voltage, and current
- Current, voltage, and resistance
- Ohm's law and basic circuit analysis
- Electrical circuits and their components
- Series and parallel circuits
- Conductors, insulators, and semiconductors
- Introduction to semiconductor devices
- Introduction to microcontrollers 


### Lecture 2 Arduino Platform: Setup, IDE & Programming Basics

Covers the Arduino UNO board in detail, walks through environment setup, and establishes a solid programming foundation using the Arduino framework.

**Topics covered:**

- Exploring Arduino and Their Diffirent Boards
- Arduino UNO board anatomy (pins, power, reset, LED)
- Installing and configuring Arduino IDE 2.x
- Connecting the board, selecting port and board type
- Writing and uploading your first sketch 
- `setup()` and `loop()` explained
- Variables and data types (`int`, `float`, `bool`, `char`, `String`)
- Arithmetic and comparison operators
- Control flow `if / else`, `for`, `while`

### Lecture 3 GPIO, Sensors, Actuators & Motors
Covers reading and driving digital and analogue pins, generating PWM signals, and working with a range of sensors, output components, and motor types.

**Topics covered:**

**GPIO Digital & Analogue**
- `digitalWrite()` / `digitalRead()` output and input modes
- Pull-up and pull-down resistors (`INPUT_PULLUP`)
- `analogRead()`  ADC (10-bit, 0–1023)
- `analogWrite()` PWM on supported pins
- PWM frequency and duty cycle explained

**Sensors & Output Components**
- Ultrasonic distance sensor (HC-SR04)
- Obstacle sensor
- Fire Sensor
- Light-dependent resistor (LDR)
- Push buttons and debouncing
- LED control (digital + PWM brightness)
- Buzzer and noise generation

**Motors**
- DC motors H-bridge driver (L298N), speed and direction control
- Servo motors `Servo.h` library, angle control
- Stepper motors full-step and half-step modes, `Stepper.h`
- Brushless DC motors ESC calibration and control via PWM

### Lecture 4 Displays, Communication Protocols & Wireless
Covers the main display technologies used with Arduino, then systematically works through each serial communication protocol, including wireless modules.

**Topics covered:**

**Display Devices**
- LED dot matrix MAX7219 driver, `LedControl` library
- 7-segment display common cathode/anode, multiplexing
- LCD 16×2 parallel wiring and I²C backpack (`LiquidCrystal_I2C`)

**Communication Protocols**

| Protocol | Speed | Wires | Use case |
|---|---|---|---|
| UART / Serial | Up to 115200 baud | 2 (TX/RX) | Debugging, modules |
| I²C | 100–400 kHz | 2 (SDA/SCL) | Sensors, displays |
| SPI | Up to 10 MHz | 4 (MOSI/MISO/SCK/SS) | SD cards, displays |

**Wireless Modules**
- HC-05 Bluetooth module AT commands, pairing, UART bridge
- ESP8266 Wi-Fi module AT firmware, connecting to a network, HTTP requests

### Lecture 5 ATmega328P Low-Level Programming & Register Configuration
This lecture leaves the Arduino library behind and programs the ATmega328P using memory-mapped registers the same way professional embedded firmware is written.

**Topics covered:**

**Architecture & Memory Map**
- ATmega328P block diagram ALU, registers, flash, SRAM, EEPROM
- I/O register addressing `DDRx`, `PORTx`, `PINx`
- Bit manipulation `|=`, `&=`, `~`, `^`, `<<`, `>>`

**Peripheral Configuration via Registers**
- GPIO configuration without `pinMode()` / `digitalWrite()`
- Timer/Counter registers  `TCCR0A/B`, `OCR0A`, prescaler selection
- ADC registers `ADMUX`, `ADCSRA`, single-conversion mode
- External interrupts `INT0 / INT1`, `EICRA`, `EIMSK`, ISR macros

**Writing Clean Embedded C**
- Functional programming style in embedded C
- Creating and using custom header files (`.h`)
- `#define`, `#ifndef` guards, `volatile` keyword


## Prerequisites

- No prior programming experience required Lectures 1 and 2 build from scratch
- Arduino UNO board (or compatible clone) + USB-B cable
- Basic electronics kit: breadboard, jumper wires, assorted resistors and LEDs
- Sensors and components listed per lecture (HC-SR04, servo, stepper, HC-05, LCD, etc.)
- [Arduino IDE 2.x](https://arduino.cc/en/software) installed


## 🗺 Learning Path

Each lecture builds directly on the one before it.

```
[L1] Electricity & Electronics
         ↓
[L2] Arduino Platform & C Basics
         ↓
[L3] GPIO · Sensors · Motors
         ↓
[L4] Displays · Protocols · Wireless
         ↓
[L5] ATmega328P Registers & Bare-Metal C
```

**Lecture 1** gives you the physics intuition that makes electronics make sense.  
**Lecture 2** grounds that theory in a real board and a working development environment.   
**Lecture 3** puts I/O at the centre reading the physical world and driving real actuators.   
**Lecture 4** expands your toolkit to displays and multi-device serial communication.    
**Lecture 5** closes the loop you learn what the Arduino library has been doing for you all along, then write it yourself.    


*© 2026  All rights reserved*
