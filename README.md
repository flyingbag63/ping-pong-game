In this project, I will show how to make a simple ping pong game using Arduino.

#Table of Contents
Introduction
Concept of ping pong game using Arduino
Circuit diagram
  Components Required
  Circuit Desgin
Code
Working of ping pong game using Arduino

##Introduction

Pong is one of the earliest arcade video games. It is a table tennis sports game featuring simple two-dimensional graphics.

##Concept of ping pong game using Arduino

I have used "|" to represent player's paddle and "." to represent ball.

##Circuit Diagram

The curcuit diagram is attached with the submission file.

###Components Required

Arduino Uno R3 
LCD 16X2
220 Ω resistor
Pushbutton (4)
1 KΩ resistor
250 KΩ potentiometer
Breadboard

###Circuit Design

Connect the 4,5,6,7 pins of the LCD to the 5,4,3,2 pins of the arduino
Connect E and R/S pins of LCD to 11 and 12 pins of the arduino
Connect 4 pushbuttons to 6,7,8,9 pins of the arduino through positive rail of the breadboard, 1 kΩ resistor and negative rail of the breadboard
Connect R/W,VCC and GND pins of the LCD to negative,positive and negative rails on the breadboard
Connect 5V power of the arduino to the positive rail and GND to the negative rail of the breadboard


##Code

The code uses custom designed characters(gylph) for the LCD. Each character in a LCD is made up of (8x5) pixels. Upto 8 characters are supported. Use createChar() to create a custom character and write() to write that character to the LCD
To create a custom character, declare a byte array of size 8, one for each row. The five least significant bits of each byte determine the pixels in that row, if the value of a pixel is 1, it means that that pixel is on, otherwise it is off
The hardest part of the code is to understand ball mechanics. It uses basic trignometry. Read the code to understand the mechanics better.


##Working of ping pong game using Arduino

After making all the connections as per the circuit diagram, upload the code to Arduino and power on the circuit.
The moment the power is turned ON, the game begins by displaying START GAME on the LCD. 
Pressing any button will start the game.
After a player scores 5 (MAX_SCORE can be modified in the code) points, the game ends.