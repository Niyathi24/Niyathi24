# Intelligent Digital Thermometer

## Overview

**Real-time Temperature Monitoring System with Embedded Interfaces**

This project implements a complete digital thermometer system using an ATmega328P microcontroller that displays ambient temperature on both a laptop serial monitor and an SSD1306 OLED display. The system features temperature unit conversion (Fahrenheit/Celsius) via push-button control and includes visual alerting through an LED when temperatures exceed configurable thresholds.

## Hardware Architecture

**Microcontroller:** ATmega328P (Arduino Uno)  
**Sensor:** TMP36 Analog Temperature Sensor (10mV/°C, 750mV at 25°C)  
**Display:** SSD1306 OLED (I2C interface, 128×64 resolution)  
**Input:** SPST momentary push-button switch  
**Alert:** Red LED with current-limiting resistor  
**Communication:** UART for serial monitor output at 9600 baud

## Implementation Approach

### Peripheral Integration Strategy
1. **Analog Sensing:** TMP36 connected to ADC pin with voltage-to-temperature conversion
2. **User Interface:** Push-button with internal pull-up resistor for unit selection
3. **Visual Display:** Dual-output system (OLED + Serial Monitor) with synchronized updates
4. **Alert System:** Threshold-based LED activation with configurable "Too Hot" values
5. **Timing Control:** 1-second sampling interval for stable readings

### Core Functionality
- **Temperature Conversion:** Raw ADC values → Voltage → Celsius → Fahrenheit
- **Unit Toggle:** Button-pressed = Celsius, Button-released = Fahrenheit
- **Dual Display:** Real-time updates on both OLED and serial monitor
- **Threshold Detection:** LED illumination at configurable temperature limits
- **Precision Format:** 0.1-degree resolution with unit suffix (e.g., "72.3F", "22.7C")

## Technical Specifications

### Temperature Calculation Pipeline
```
ADC Reading → Voltage (0-5V) → Celsius (°C) → Fahrenheit (°F)
           V_REF/1023 * digitalValue → (Voltage - 0.5)/0.01 → °C × 9/5 + 32
```

### System Configuration
- **ADC Reference:** 5V (V_REF)
- **Sampling Rate:** 1 Hz
- **Display Precision:** 1 decimal place
- **Threshold Testing:** 60°F and 80°F "Too Hot" values
- **Button Logic:** Active-low with internal pull-up

### Library Integration
- **SSD1306 & I2C:** OLED display control and communication
- **my_adc_lib:** Analog-to-digital conversion for TMP36 sensor
- **my_uart_lib:** Serial communication for laptop display
- **Makefile Management:** Multi-file compilation with user-contributed libraries

## Key Results & Features

| Component | Implementation | Functionality |
|-----------|----------------|---------------|
| **Dual Display** | OLED + Serial Monitor | Synchronized temperature display |
| **Unit Conversion** | Button-controlled toggle | Instant °C/°F switching |
| **Alert System** | Threshold-based LED | Visual "Too Hot" indication |
| **Precision** | 0.1-degree resolution | Accurate temperature reporting |
| **Timing** | 1-second intervals | Stable, readable updates |

### Performance Characteristics
- **Response Time:** <1 second for display updates
- **Accuracy:** ±1°C within TMP36 specifications
- **Reliability:** Debounced button readings, filtered ADC values
- **Usability:** Clear dual-display with intuitive unit switching

## Technologies & Skills

**Embedded C Programming:** Peripheral control, interrupt-free polling, real-time systems  
**Hardware Interfaces:** I2C (OLED), ADC (TMP36), GPIO (Button/LED), UART (Serial)  
**Sensor Integration:** Analog temperature sensing, calibration, linear conversion  
**Display Systems:** Bitmap graphics (OLED), serial terminal communication  
**System Integration:** Multi-peripheral coordination, timing management, power considerations

## Impact

This project demonstrates:
- **Full-stack embedded development** from schematic to functional system
- **Multi-interface coordination** between analog, digital, and serial communications
- **Real-world sensor implementation** with practical calibration and conversion
- **User-centric design** through intuitive controls and dual feedback mechanisms
- **Robust error handling** in resource-constrained embedded environments
