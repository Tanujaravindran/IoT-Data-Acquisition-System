# IoT-Data-Acquisition-System
An embedded IoT data acquisition system developed using ARM microcontroller, UART, SPI, LCD interfacing, and WiFi communication for real-time sensor data monitoring and transmission.
# IoT-Based Temperature Monitoring and Cloud Monitoring System

## Overview

This project implements an IoT-based Temperature Monitoring and Cloud Monitoring System using the LPC2129 ARM7 microcontroller. The system continuously acquires temperature data from an LM35 temperature sensor, converts the analog signal into digital form using the MCP3208 ADC, displays the temperature locally on a 16x2 LCD, and uploads the data to the ThingSpeak cloud platform through an ESP8266 WiFi module for remote monitoring.

## Objectives

* Monitor temperature in real time.
* Display temperature locally on an LCD.
* Upload temperature data to the cloud.
* Enable remote monitoring through the Internet of Things (IoT).

## Hardware Components

* LPC2129 ARM7 Microcontroller
* LM35 Temperature Sensor
* MCP3208 12-bit ADC
* ESP8266 ESP-01 WiFi Module
* 16x2 LCD Display
* Power Supply Circuit

## Software Tools

* Embedded C
* Keil uVision IDE
* Flash Magic
* ThingSpeak Cloud Platform

## Communication Protocols Used

### SPI Communication

SPI is used for communication between the LPC2129 microcontroller and MCP3208 ADC. The ADC converts the analog voltage from the LM35 sensor into digital values which are processed by the microcontroller.

### UART Communication

UART is used for communication between the LPC2129 microcontroller and ESP8266 WiFi module. AT commands are transmitted to establish WiFi connectivity and upload data to the cloud.

## Working Principle

1. The LM35 sensor measures ambient temperature.
2. The MCP3208 ADC converts the analog sensor output into digital data.
3. LPC2129 reads the ADC value using SPI communication.
4. Temperature is calculated and displayed on the LCD.
5. The ESP8266 WiFi module is initialized using AT commands.
6. Temperature data is transmitted to the ThingSpeak cloud platform.
7. Users can monitor live temperature data remotely through the ThingSpeak dashboard.

## Project Architecture

LM35 Sensor
↓
MCP3208 ADC
↓ (SPI)
LPC2129 Microcontroller
↓
16x2 LCD Display

LPC2129
↓ (UART)
ESP8266 WiFi Module
↓
ThingSpeak Cloud
↓
Remote Monitoring Dashboard

## Source Files

* main.c – Main application logic
* SPI_header.h – SPI communication and ADC reading
* UART_header.h – UART0 communication functions
* UART1_header.h – UART1 communication functions
* wifi.c – ESP8266 initialization and ThingSpeak data upload
* wifi_header.h – WiFi function declarations
* lcd_4bit.h – LCD interface driver
* delay_header.h – Delay functions

## Features

* Real-time temperature monitoring
* LCD-based local display
* Cloud-based remote monitoring
* WiFi connectivity using ESP8266
* SPI and UART communication implementation
* Low-cost embedded IoT solution

## Applications

* Industrial Monitoring
* Smart Agriculture
* Weather Monitoring
* Data Logging Systems
* Home Automation
* Healthcare Monitoring

## Future Enhancements

* Mobile App Integration
* SMS/Email Alerts
* Multi-Sensor Monitoring
* Data Analytics Dashboard
* Predictive Maintenance Features

## Author

Tanuja B.R.

Aspiring Data Analyst | Embedded Systems & IoT Enthusiast
