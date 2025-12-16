# **Weather Microground: Low-Power Embedded Weather Station**

## Problem Statement
Design and build a compact, low-power weather station using Nordic Thingy52 and 2.13" ePaper display that provides meaningful weather statistics through historical data analytics without cloud dependency or constant internet connectivity.

## Key Requirements
- **Sensing:** Continuous temperature, humidity, and pressure monitoring
- **Display:** 2.13" monochrome ePaper display with three visualization contexts
- **Power Efficiency:** Optimized sampling and refresh rates for extended battery life
- **Local Analytics:** Historical data processing and trend analysis without cloud dependency
- **User Interface:** Push-button navigation between display contexts

## System Architecture

### Hardware Components
- **Microcontroller:** Nordic Thingy52 (nRF52832)
- **Sensors:** Integrated temperature, humidity, pressure sensors
- **Display:** 2.13" monochrome ePaper display
- **Interface:** Single push-button for context cycling

### Software Design
- **Real-time Sensing:** 30-second sampling interval
- **Display Management:** 60-second refresh rate
- **Data Storage:** Circular buffers for 1-hour historical data
- **Three Visualization Contexts:**
  - **Context 0:** Current values with 1-hour statistics (mean ± std dev)
  - **Context 1:** Temperature trend bar graph over last hour
  - **Context 2:** Storm prediction based on pressure trends

## Technical Implementation

### Power Optimization

- **Balanced Sampling:** 30-second intervals capture meaningful variations without excessive processing
- **Efficient Display:** 60-second refresh minimizes ePaper power consumption
- **Memory Management:** Optimized buffer sizes for constrained embedded environment

### Data Management

- **Circular Buffers:** 120-sample buffers store 1-hour data at 30-second intervals
- **Statistical Analysis:** Real-time computation of mean and standard deviation
- **Efficient Storage:** Optimized for Thingy52 memory constraints

### Visualization Contexts

#### Context 0: Real-time Statistics
- Displays current temperature, humidity, pressure
- Shows 1-hour standard deviation for each metric
- Provides immediate environmental awareness with historical context

#### Context 1: Temperature Trends
- Bar graph visualization of hourly temperature data
- Automatic scaling based on min/max values
- Visual representation of temperature fluctuations

#### Context 2: Storm Prediction

- **Pressure-based heuristic:** 2.0 hPa drop threshold for storm prediction
- **Simple but effective:** Rapid pressure drops indicate severe weather
- **Real-time analysis:** Compares current pressure with 1-hour old data

## Performance Analysis

### Key Design Decisions
- **Buffer Size:** 120 samples balances memory usage and analytical capability
- **Sampling Rate:** 30-second intervals provide adequate temporal resolution
- **Refresh Rate:** 60-second updates balance responsiveness and power consumption
- **Storm Threshold:** 2.0 hPa drop based on meteorological principles

### Technical Challenges
- **Memory Constraints:** Optimized data structures for limited RAM
- **Power Management:** Balanced sensing frequency with battery life
- **Display Optimization:** Managed ePaper refresh cycles for readability and efficiency
- **Real-time Processing:** Efficient statistical computation on embedded hardware

## Validation
- **Context 0:** Verified statistical calculations against reference measurements
- **Context 1:** Confirmed temperature trend accuracy with known test patterns
- **Context 2:** Validated storm prediction logic against meteorological data
- **Power Performance:** Achieved target battery life through optimized timing
- **User Experience:** Seamless context switching with responsive interface

## Technologies Used
- **Platform:** Nordic Thingy52 (nRF52832)
- **Sensors:** Integrated environmental monitoring
- **Display:** 2.13" ePaper with SPI interface
- **Language:** C

## Team Contributors
- **Sreeniyathi Kasireddy**
- **Ananya Rohatgi**
- **Samanvay Upadhyay**
