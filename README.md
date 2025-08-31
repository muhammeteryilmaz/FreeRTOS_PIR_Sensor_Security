# FreeRTOS_PIR_Sensor_Security

## Description
This project implements a security system using a PIR (Passive Infrared) sensor to detect motion. When motion is detected, an interrupt triggers a FreeRTOS binary semaphore, activating a task that turns on an LED and a buzzer for 1 second.

## FreeRTOS Features
- Binary semaphore (`xSemaphoreCreateBinary`, `xSemaphoreGiveFromISR`, `xSemaphoreTake`)
- Interrupt management (`portYIELD_FROM_ISR`)
- Task management

## Hardware
- **Microcontroller**: STM32F446ZET6
- **PIR Sensor**: Connected to PB8 (interrupt on rising/falling edge, pull-down resistor)
- **LED**: Onboard LED on PB7 (with integrated resistor)
- **Buzzer**: Connected to PB9

## Setup
1. Open the project in STM32CubeIDE.
2. Ensure FreeRTOS and HAL libraries are included.
3. Connect the PIR sensor to PB8, LED to PB7, and buzzer to PB9.

## Outputs
- **LED and Buzzer**: Turn on for 1 second when motion is detected

## Test Results
- The PIR sensor triggered interrupts successfully after adjusting the time delay potentiometer. The LED and buzzer activated as expected.
