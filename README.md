# STM32F411 Nucleo ADC Potentiometer Reader

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue)
![ADC](https://img.shields.io/badge/ADC1-Single_Conversion-green)



Read potentiometer values using ADC1 in single conversion mode.

## Features
- **12-bit ADC Resolution** (0-4095 range)
- **PA0 Analog Input** for potentiometer
- **Polling Mode** conversion
- **84MHz System Clock** (HSI-based PLL)

## Hardware Setup
| Component | Connection | Nucleo Pin |
|-----------|------------|------------|
| Potentiometer | VCC → 3.3V | - |
| | GND → GND | - |
| | WIPER → PA0 | CN7 pin 10 |

## Technical Details
### ADC Configuration (RM0383 §13)
```c
Clock: 21MHz (84MHz PCLK2 / 4)
Channel: ADC1_IN0 (PA0)
Sampling Time: 3 ADC cycles
Trigger: Software
