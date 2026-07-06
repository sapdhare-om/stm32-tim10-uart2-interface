# STM32 TIM10 and USART2 Interfacing using Polling

## Overview

This project demonstrates the interfacing of **TIM10** and **USART2** on the **STM32 NUCLEO-F401RE** using **STM32CubeMX**, **STM32CubeIDE**, and **Proteus**.

The objective is to transmit the message **"Welcome"** on **USART2** every **3 seconds** by using **TIM10 in Polling Mode** instead of software delay (`HAL_Delay()`).

This project was developed as part of an **ARM-Based Embedded Systems** practical.

---

## Project Objective

- Configure **TIM10** as a base timer.
- Configure **USART2** for serial communication.
- Generate a **3-second delay** using TIM10 polling.
- Transmit the message **"Welcome"** continuously through UART.
- Simulate the project in Proteus.

---

## Hardware Used

- STM32 NUCLEO-F401RE
- USB Cable
- PC/Laptop

---

## Software Used

- STM32CubeMX
- STM32CubeIDE
- Proteus 8 Professional

---

## Peripherals Used

- TIM10 (Timer)
- USART2 (UART)

---

## Timer Configuration

| Parameter | Value |
|-----------|--------|
| System Clock | 16 MHz |
| Prescaler | 15999 |
| Auto Reload Register (ARR) | 2999 |
| Counter Mode | Up Counter |
| Clock Source | Internal Clock |

---

## Timer Calculation

Timer Clock = 16 MHz

Prescaler = 15999

Timer Frequency

```
16,000,000 / (15999 + 1)
= 1000 Hz
```

Time per Count

```
1 / 1000
= 1 ms
```

Counter Period

```
2999 + 1
= 3000 Counts
```

Delay

```
3000 × 1 ms
= 3 Seconds
```

---

## Project Flow

```
STM32CubeMX
        │
        ▼
Code Generation
        │
        ▼
STM32CubeIDE
        │
        ▼
Compile & Generate HEX
        │
        ▼
Proteus Simulation
        │
        ▼
Virtual Terminal Output
```

---

## Output

```
Welcome

Welcome

Welcome
```

The message is transmitted every **3 seconds** through USART2.

---

## Learning Outcomes

- STM32CubeMX Peripheral Configuration
- UART Communication using HAL Library
- Timer Configuration using Polling
- Clock Configuration and Timer Calculations
- Proteus Simulation
- Embedded System Debugging Techniques

---

## Challenges Faced

- Configuring TIM10 correctly.
- Understanding timer calculations.
- Debugging UART communication.
- Verifying timer overflow using polling.
- Integrating TIM10 with USART2 successfully.

---

## Future Improvements

- Implement the project using **Timer Interrupts**.
- Display UART data on an LCD.
- Add FreeRTOS-based task scheduling.
- Extend the project using DMA for UART transmission.

---

## Author

**Om Gajanan Sapdhare**

---

## License

This project is shared for educational and learning purposes.
