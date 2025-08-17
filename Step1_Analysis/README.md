# Step 1 : Problem Understanding and Analysis

## Problem Definition

A food shelter needs an automated pet feeder to be designed which dispenses food for cat and dog at scheduled intervals. It checks if the food has been dispensed and the amount of food that has been consumed. The system must send an alert incase of any issue like food not dispensed or consumed.

## Features

    1. The feeder channel must be opened periodically as per the system clock.
    2. Weight of the bowl must be monitered regularly and if food is not consumed, the alert must be given.
    3. The food bowl must be monitered to ensure that food is dispensed.
    4. The food stock must be monitered before and after each dispense to ensure food is always present in the feeder.

## Inputs and Outputs

### Inputs:

    1. Feeding Schedule
    2. System Time
    3. Food Weight Sensor
    4. Food Stock weight
    5. Maximum consumption Time


### Outputs

    1. Control signal for sensor for opening/closing food channel.
    2. Alert LEDS (Red LED on or off indicating food in the bowl).
    3. Buzzer for alert.

### Assumptions and Limitations

    1. Only one type of food is dispensed ensuring consistent food size and weight.
    3. Only one feeding bowl.
    3. Food is dispensed everyday at 8 AM and 6 PM(18:00).
    4. The minimum and maximum amount of food to be present in the bowl must be set by the user to define bowl full and bowl empty conditions.
    5. After the food is dispensed, if the food is not consumed (the weight of the feeding bowl remains constant) then alert a "Food not consumed" alert through a red LED and buzzer on the system then waits for an hour and checks the weight of the bowl again.
    6. In the case of an overflow of food (weight of food is higher than the upper threshold set) then a red LED with a buzzer is triggered which requires manual attention.
    7. In the case of food not dispensed, an alert with red LED is triggered after which manual attention is required.
    8. The system comes to an end only when the power is manually turned off, else the system continues to execute in a loop as per the clock.

## System Diagram

![alt text](<Block diagram.drawio (1).png>)
