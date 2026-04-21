# GridMinds - Smart Grid Voltage Monitor & Protection System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Raspberry%20Pi%20Pico-brightgreen)](https://www.raspberrypi.com/products/raspberry-pi-pico/)

## 📋 Overview

GridMinds is an intelligent voltage monitoring and protection system designed for the Raspberry Pi Pico. It simulates real-world grid voltage monitoring using a potentiometer as an input source, with automatic load disconnection during unsafe voltage conditions (overvoltage/undervoltage). The system provides visual feedback via an onboard LED and controls a relay to protect connected equipment.

## 🎯 Use Case

This system is ideal for:
- **Educational demonstrations** of grid protection mechanisms
- **Testing environments** where real grid voltages need simulation
- **Prototype development** for industrial voltage monitoring systems
- **Home automation** projects requiring voltage threshold monitoring

## ⚡ Key Features

- **Real-time voltage monitoring** with 0.1V precision
- **Programmable voltage thresholds** (Default: 216V-254V for UK/EU/AU standards)
- **Automatic load disconnect** during voltage anomalies
- **Chatter prevention** with stabilization delays
- **Visual status indication** via onboard LED
- **Simulated voltage input** (0-300V range via potentiometer)

## 🔧 Hardware Requirements

| Component | Pin | Description |
|-----------|-----|-------------|
| Raspberry Pi Pico | - | Microcontroller board |
| Potentiometer | GP26 (ADC0) | Simulates grid voltage (0-300V) |
| Relay Module | GP15 | Controls load connection |
| LED (Optional) | GP25 | Visual status indicator (onboard) |

## 📊 Voltage Standards

The system is pre-configured for UK/EU/AU grid standards (230V +10%/-6%):

- **Maximum safe voltage**: 224V (trips above this)
- **Minimum safe voltage**: 216V (trips below this)
- **Simulation range**: 0-300V (potentiometer full range)

## 🚀 Installation & Setup

### 1. Hardware Connections
```bash
Potentiometer:
  - Left pin  → 3.3V
  - Middle pin → GP26 (ADC0)
  - Right pin  → GND

Relay Module:
  - Signal → GP15
  - VCC    → 3.3V/5V (check module specs)
  - GND    → GND
