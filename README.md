# STM32 LED Blinking using HAL

## Project Overview

This is my first STM32 embedded systems project using the STM32F103C8T6 Blue Pill development board.

The objective of this project is to understand GPIO configuration and control an onboard LED using the STM32 Hardware Abstraction Layer (HAL).

The LED is toggled at 500 millisecond intervals using the HAL library.

## Hardware Requirements

- STM32F103C8T6 Blue Pill development board
- ST-Link V2 programmer/debugger
- USB cable
- Computer

## Software Requirements

- STM32CubeIDE 2.2.0
- STM32CubeMX 6.18.1
- STM32 HAL Library

## GPIO Configuration

| Parameter | Configuration |
|---|---|
| Microcontroller | STM32F103C8T6 |
| GPIO Port | GPIOC |
| GPIO Pin | PC13 |
| Mode | GPIO Output Push-Pull |
| LED Toggle Interval | 500 ms |

## Embedded C Implementation

The LED blinking functionality uses two HAL functions:

**1. HAL_GPIO_TogglePin()**

Toggles the output state of the selected GPIO pin.

```c
HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_13);
```

**2. HAL_Delay()**

Introduces a delay of 500 milliseconds.

```c
HAL_Delay(500);
```

These functions are executed repeatedly inside the main application loop.

## How It Works

1. Configure PC13 as GPIO Output Push-Pull using STM32CubeMX.
2. Initialize the STM32 HAL and GPIO peripherals.
3. Toggle the GPIO output state.
4. Wait for 500 milliseconds.
5. Repeat the process continuously.

## Project Structure

```text
LED_BLINK/
│
├── Drivers/
├── Inc/
├── Src/
├── Startup/
├── .gitignore
├── LED_BLINK.ioc
├── .project
├── .cproject
└── STM32F103C8TX_FLASH.ld
```

## Build and Flash

1. Open the project in STM32CubeIDE.
2. Build the project.
3. Connect the ST-Link V2 programmer to the Blue Pill.
4. Flash the firmware onto the STM32.
5. Run the program and observe the onboard LED.

## Project Results

- Successfully configured PC13 as GPIO Output Push-Pull.
- Successfully implemented LED toggling using STM32 HAL.
- Successfully built the project with zero errors and zero warnings.
- Successfully debugged and flashed the firmware.
- Verified that the onboard LED blinks.

## Learning Outcomes

Through this project, I learned:

- STM32 project creation and configuration.
- GPIO output configuration.
- Basics of Embedded C programming.
- STM32 HAL functions.
- Building and debugging firmware.
- Flashing programs using ST-Link V2.
- Basic GitHub project management.

## Author

Embedded Systems Learner

## License

This project is available for educational and learning purposes.
