# Hexapod-PCB
### 4-Layer PCB for the Arduino Hexapod

## Introduction
This PCB is a 4-Layer hexapod for servo applications. It containes a signal layer for all the servo pwm pins and a uniform ground + power plane for the servos spesifically. The reason while I decided to go through this project is because I wanted a way that I can adjust the voltage level of the servos as depending on the voltage of the servos the speed and tourque is affected. This also will organize my wire managment by a lot since I don't have to extrapolate my electonics to a bunch of breadboards.

## Goals
Here are the main goals of this PCB:
- Make a PCB that can manage 18 seperate servos simutaneously.
- Have uniform and stable power for all 18 servos.
- Make calculations using a inertial sensor for inverse kinematics.
- Use NRF protocol to communicate with a RC transmitter.
- Have indication for the hexapod status using LEDs and a Buzzer.
## PCB 3D Model

<img width="1250" height="896" alt="Screenshot 2025-07-10 184733" src="https://github.com/user-attachments/assets/4739cc6b-deb9-4032-8c8e-eddbcf8b6957" />

## PCB Picture

<img width="1371" height="913" alt="Screenshot 2025-07-10 184709" src="https://github.com/user-attachments/assets/2cde1c28-1cb7-4622-bc23-148b889e70aa" />

##Bill of Materials
| Item Name                | Price (USD) | Quantity | Total Price (USD) | Purchase Link                                                                                           |
| ------------------------ | ----------- | -------- | ----------------- | ------------------------------------------------------------------------------------------------------- |
| PCB Order                | \$48.73     | 1        | \$48.73           | [PCBWay](https://www.pcbway.com/QuickOrderOnline.aspx)                                                  |
| Teensy 4.1               | \$40.83     | 1        | \$37.50           | [Amazon](https://www.amazon.com/PJRC-Cortex-M7-Processor-iMXRT1062-Without/dp/B088JY7P2H)               |
| Male Pin Header Strips   | \$8.99      | 1        | \$8.99            | [Amazon](https://www.amazon.com/Straight-Breakaway-Connector-Breadboard-Electronic/dp/B09MYBRW3F)       |
| Female Pin Header Strips | \$12.98     | 1        | \$12.98           | [Amazon](https://www.amazon.com/Exclusive-2-54mm-1x42pin-2x42pin-Break-Away/dp/B0BK87GBM3)              |
| 7.4V 5200mAh LiPo        | \$15.97     | 1        | \$15.97           | [Amazon](https://www.amazon.com/Zeee-5200mAh-Battery-Truggy-Airplane/dp/B06ZYRCPS3)                     |
| ACS712 Current Sensor    | \$2.92      | 2        | \$5.84            | [DigiKey](https://www.digikey.com/en/product-highlight/a/allegro-microsystems/acs712-current-sensor-ic) |
| WS2812B Individual LEDs  | \$0.85      | 2        | \$1.70            | [DigiKey](https://www.digikey.com/en/products/detail/sparkfun-electronics/COM-24837/22321085)           |
| Logic Shifter            | \$7.49      | 1        | \$7.49            | [Amazon](https://www.amazon.com/HiLetgo-Channels-Converter-Bi-Directional-3-3V-5V/dp/B07F7W91LC)        |
| 10pc Buzzers             | \$6.99      | 1        | \$6.99            | [Amazon](https://www.amazon.com/mxuteuk-Electronic-Computers-Printers-Components/dp/B07VK1GJ9X)         |
| OLED Display             | \$14.99     | 1        | \$14.99           | [Amazon](https://www.amazon.com/Hosyond-Display-Self-Luminous-Compatible-Raspberry/dp/B09T6SJBV5)       |
| ** Total Cost**        |             |          | **\$146.19**      |                                                                                                         |
