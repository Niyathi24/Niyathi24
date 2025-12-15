# WaveMix: E-textile Gesture-Based DJ Control System
**Status:** In Progress (Started September 2025) 

## Overview

WaveMix is an innovative e-textile DJ control system that translates hand gestures into real-time audio manipulation, enabling musicians to mix and modify music through natural physical movements. This ongoing project combines embedded hardware design, real-time sensor processing, and web-based audio synthesis to create an accessible, performance-ready wearable interface.

## Problem Statement

**How can we create an intuitive, low-cost wearable interface that translates expressive hand gestures into professional-grade audio control with minimal latency?**

This project addresses the challenge of bridging physical gesture recognition with digital audio processing in a resource-constrained wearable format, requiring optimization across hardware, firmware, and software layers.

## System Architecture

### Hardware Stack
- **Microcontroller:** ESP32 (BLE + Wi-Fi capabilities)
- **Sensors:** Force-Sensitive Resistors (FSR), Flex sensors
- **Power:** LiPo battery with power management IC
- **Connectivity:** Bluetooth Low Energy (BLE) for sensor data streaming

### Software Pipeline
```
Gesture → Sensors → ESP32 → BLE → WebSocket → Web Audio API → Audio Output
```

## Technical Implementation

### Core Subsystems

**1. Audio Processing Engine (Web Audio API)**
- Real-time audio synthesis and effect processing
- Low-latency parameter modulation via gesture inputs
- Multi-channel mixing with visual feedback interface
- Custom audio node graph for effect chaining

**2. Sensor Data Pipeline**
- BLE advertising at 20ms intervals for motion data
- WebSocket bridge for browser compatibility
- Sensor fusion algorithms for gesture recognition
- Calibration routines for user-specific adjustments

**4. Hardware Design Constraints**
- Total BOM cost target: <$200
- Battery life: 2+ hours continuous operation
- Latency budget: <50ms end-to-end
- Form factor: Hand-worn textile with minimal bulk

## Current Development Status

**Phase 1:** Hardware prototyping and basic sensor integration  
**Phase 2:** Web Audio API implementation and BLE communication  
**Phase 3:** Optimization and latency tuning  
**Phase 4:** User testing and performance validation  
**Next Milestone:** Integrating more sensors and features to the glove

## Technologies & Skills

**Embedded Systems:** ESP32 programming, BLE protocol, power management, sensor interfacing  
**Web Technologies:** Web Audio API, WebSockets, real-time data visualization, React frontend  
**Hardware Design:** PCB layout (KiCad), prototyping, testing  
**Project Management:** Budget tracking, component procurement, timeline management, team coordination

## Expected Impact & Applications

**DJ:** Enhanced DJ interface for expressive performance  
**Accessibility:** Alternative control system for users with limited mobility  
**Education:** Teaching tool for interactive music and embedded systems  
**Research Platform:** Framework for studying human-computer interaction through wearables
