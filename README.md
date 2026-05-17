# Arduino LED Blinking using Embedded C (Register-Level Programming)

This project demonstrates LED blinking on an Arduino UNO using direct register programming in Embedded C instead of high-level Arduino functions.

## Objective
To understand low-level microcontroller programming using:
- DDRB register
- PORTB register
- Bitwise operations

## Hardware Used
- Arduino UNO
- LED
- 220Ω Resistor
- Breadboard
- Jumper wires
- USB cable

## Circuit Connection

Digital Pin 12 --> resistor(220) --> LED(+) 
LED(-) --> GND

## Code
void setup(){
  DDRB |= (1 << 4);
}

void loop(){
  PORTB |= (1 << 4);
  delay(1500);

  PORTB &= ~(1 << 4);
  delay(1500);
}
