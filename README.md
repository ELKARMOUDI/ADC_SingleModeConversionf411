# STM32F411 Nucleo ADC Potentiometer Reader

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue)
![ADC](https://img.shields.io/badge/ADC1-Single_Conversion-green)

<img src="https://github.com/user-attachments/assets/4d517824-49ef-4cd8-b0d3-77b2f7c27de5" width="400" alt="6A330F06-8B40-4DF4-938F-0E164BC30F8F">

<img src="https://github.com/user-attachments/assets/49d00764-7fd7-480c-ae10-18894e83da84" width="400" alt="90E4A16F-0D16-46A5-A932-427F3E33BAFC">

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
### ADC Configuration 
```c
Clock: 21MHz (84MHz PCLK2 / 4)
Channel: ADC1_IN0 (PA0)
Sampling Time: 3 ADC cycles
Trigger: Software
