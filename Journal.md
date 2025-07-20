---
title: "Hexapod PCB"
author: "Chinedu Okpala"
description: "4-Layer PCB for Robotic hexapod"
created_at: "2025-6-26"
---
# 4-Layer Hexapod PCB.

##Total Hours: 21

## Reaserch 6/26/2025 3 Hours

In order to create a 4-layer PCB, I knew that I needed to first look into how I should go about it. The main reason why I wanted to use a 4-layer board was due to two factors:

- Uniform power distribution for all 18 servos.
- Space for all the traces on the pcb.

Uniform power planes allow for better power distribution while also protecting signal integrity to some degree. After looking into different configurations, I decided to layer my 4-layer PCB as this:

1. Signal
2. Ground
3. Power
4. Back

This formation allows me to protect the main signal integrity of the servos due to it being near the ground plane. Thats the main thing but the back also allows me to do leftover traces.

## Circuit Schematic 6/27/2025 - 6/28/2025 6 Hours

This circuit diagram took quite the time due to stuff from my past arduino shield needing to be revamped. The one thing that stayed constant was the pins schematic that I could just transfer over. This was the pins shcematic for the pcb:

![Screenshot 2025-07-08 015910](https://github.com/user-attachments/assets/0b1e4bd3-c929-446c-aea7-1b0c5775c379)

The next part that I decided to tackle was the arduino mega pro that I would be using. All I needed to do was to look at an arduino mega pro 2560 as a refrence to see the best possible routing digital pins. This was fairly simple and after adding additional analog pins that I would be using later, this was the arduino mega pro schematic:

![Screenshot 2025-07-08 020239](https://github.com/user-attachments/assets/d9019444-f72f-4b7c-aaff-d7cf27fffa84)

The next step was the NRF2401+. The datasheet recommended to use a capacitance of at least 10.1 nano farads. So I decided to simply use a 22 nf capacitor since I can use one from a cap kit that I had. Besides that it was pretty simple. This was my schematic:

![Screenshot 2025-07-08 230751](https://github.com/user-attachments/assets/b4367931-3791-4580-8144-cb187c6534c4)

The Inertial sensor (MPU6050) which I am using to deduce the accelerations of the robot is next. It was reccomended that the sda and scl connections had pull up resistors with 4.7k ohms. This was my schematic:

![Screenshot 2025-07-08 230920](https://github.com/user-attachments/assets/ef30f51e-49fd-43a7-94a2-bff455dca68d)

Looking at the indicators for my PCB (2 LEDS & 1 Buzzer) I just decided to use the first buzzer I found online due to its cheapness not affecting performances. For the LEDs I am using the WS2812B LEDs due to their multicolor features and ease of use. Besides this the LEDs also needed a ceramic cap for signal decoupling purposes. THese were the schematics for the buzzer and leds respectively:

![Screenshot 2025-07-09 020554](https://github.com/user-attachments/assets/38628f68-14e7-4aa6-a976-9e131ebe79ff)
(Buzzer)

![Screenshot 2025-07-09 020547](https://github.com/user-attachments/assets/d1961b62-34f6-4d24-8a65-7a2a8930b16e)
(LEDs)

Finally, probably the most important part is the power supply. The main thing that I need from this power supply is a constant voltage so that in cases where a sservo moving can cause a voltage disturbance or some other wacky stuff I can still get a smooth voltage. I decided to use 2 bulky capacitors that combat changes in voltage. Also some other things that I added was a voltage divider to measure voltage and a current IC to measure current. This was the power supply shcematic that I have cooked up:

![Screenshot 2025-07-09 020600](https://github.com/user-attachments/assets/8de32bee-3478-4e55-b007-b14bab794277)

## PCB Routing / Editing 6/29/25 - 7/7/2025 15 Hours

Something to note into how this part took so so long is that it went through multiple variations. The first thing I needed to do was to position all the components in a way that I could route them. This was the arrangemnt that I came up with:

![Screenshot 2025-07-09 132925](https://github.com/user-attachments/assets/cc99aba1-c0a6-4610-a25d-9eea4e4d5ae4)

Nex was the actual routing part of this PCB. But as I was thinking about the circuit I realized something: the arduino & the servos needed a different power supply. Since my arduino mega pro takes a minimum of 7V while the maximum that the servos should be getting is 6.8V, which I possibly wanted to get lower for higher speed. I decided that I would need to attach a buck converter onto the actual board. However, I was not sure which voltage to use and which speed I wanted. After I finished routing everything, this was my final PCB:

![Screenshot 2025-07-09 191733](https://github.com/user-attachments/assets/aefc109a-b351-4776-9c53-1621f2ca8f49)

## A Teensy Update 7/16/25 - 7/20/25 10 Hours
After getting my project rejected twice. I decided that I needed to change the size of the circuit board. I decided to replace the arduino mega pro with the Teensy 4.1 due to is lower size and it being a much better microcontroller. This was a simple fix as all I needed to do was look at the pwm ports on the teensy and see what I needed to swap. This was the teensy schematic I chalked up:

<img width="552" height="783" alt="Screenshot 2025-07-20 032936" src="https://github.com/user-attachments/assets/b7c359a9-160c-4af7-8886-85540c23f8e7" />

Funny thing, since the logic level was lower than the 3.5V (0.7VDD) needed, I needed to use a logic converter. I also added a OLED & 2 buttons so that I can interact with the sensors on board. Besides those fixes and the overall rerouting of the board, there was not any notable changes. This was the final schematic & 3D Model:

### PCB Layout

<img width="1176" height="1188" alt="Screenshot 2025-07-20 022511" src="https://github.com/user-attachments/assets/aa329c04-3c88-4034-b879-03c0419d44f5" />

### PCB 3D Model

<img width="1627" height="1332" alt="Screenshot 2025-07-20 023243" src="https://github.com/user-attachments/assets/cb7300b7-870b-44a2-840a-a3112d05a7e1" />


