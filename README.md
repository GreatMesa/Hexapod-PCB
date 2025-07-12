# Hexapod-PCB
### 4-Layer PCB for the Arduino Hexapod

## Introduction
This PCB is a 4-Layer hexapod for servo applications. It containes a signal layer for all the servo pwm pins and a uniform ground + power plane for the servos spesifically. The reason while I decided to go through this project is because I wanted a way that I can adjust the voltage level of the servos as depending on the voltage of the servos the speed and tourque is affected. This also will organize my wire managment by a lot since I don't have to extrapolate my electonics to a bunch of breadboards.

## Goals
Here are the main goals of this PCB
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

| Item Name                                           | Price (USD) | Quantity | Total Price (USD) | Purchase Link                                                                                                                                                                          |
| --------------------------------------------------- | ----------- | -------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| PCB Order                                           | \$95.36     | 1        | \$95.36           | [Link](https://trade.jlcpcb.com/checkout/payMethod/?unionSettleId=d344786b30a9436bb2d3a29543592d78&systemType=order_pcb&orderTypes=order_pcb&calType=PRE_CAL&spm=Jlcpcb.Partcart.1002) |
| Gold-Plated Hand Breakaway Female Pin Header Strips | \$12.98     | 1        | \$12.98           | [Link](https://www.amazon.com/Exclusive-2-54mm-1x42pin-2x42pin-Break-Away/dp/B0BK87GBM3)                                                                                               |
| 7.4V 5200mAh Lipo Battery                           | \$15.97     | 1        | \$15.97           | [Link](https://www.amazon.com/Zeee-5200mAh-Battery-Truggy-Airplane/dp/B06ZYRCPS3)                                                                                                      |
| ACS712 Current Sensor                               | \$2.92      | 2        | \$5.84            | [Link](https://www.digikey.com/en/product-highlight/a/allegro-microsystems/acs712-current-sensor-ic)                                                                                   |
| WS2812B Individual LEDs                             | \$0.85      | 10       | \$8.50            | [Link](https://www.amazon.com/Adafruit-5050-Integrated-Driver-Chip/dp/B00SK8LY9A)                                                                                                      |
| 10pc Buzzers                                        | \$6.99      | 1        | \$6.99            | [Link](https://www.amazon.com/mxuteuk-Electronic-Computers-Printers-Components/dp/B07VK1GJ9X)                                                                                          |
| 2.54 mm Single Row Male Pin Headers (20 pcs)        | \$6.99      | 1        | \$6.99            | [Link](https://www.amazon.com/HiLetgo-20pcs-2-54mm-Single-Header/dp/B07R5QDL8D)                                                                                                        |
| Molence Screw Terminal Connector Kit (26–18 AWG)    | \$10.99     | 1        | \$10.99           | [Link](https://www.amazon.com/Molence-Terminal-Connector-Terminals-26-18AWG/dp/B09F6TC7RP)                                                                                             |
| **nRF24L01 2.4 GHz Wireless Transceiver Module**    | varies      | 1        | \~\$3–\$10        | See options below                                                                                                                                                                      |
| **Total Cost (w/ cheapest wireless option)**        |             |          | **\~\$166.62**    |                                                                                                                                                                                        |
