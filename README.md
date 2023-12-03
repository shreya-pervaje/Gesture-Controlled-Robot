The project contains robot with clamper and gloves with which the gestures are given. The patients or elderly could use the gestures to control the movement of the robot and its clamper 

This file contains two different code to be burned on two different units: Gesture unit and Robot unit. 




# How to run the code
The gesture unit code "Gesture_unit.c" code is burned to the microcontroller on which is placed on the gloves and gesture sensors.

The robot unit code "Robot_unit.c" is burned to the microcontroller on the Robot unit which is build with chasis, servo motors and RF receivers. 

# What does the code do
The gestures are read from gesture sensors and its input at the analog ports of Atmega 328p controller. The values from the sensors are caliberated to read the sensor value changes and converted to digital values using ADC conversions with the help of prescalers. The values are further processed and encoded before sending it to RF transmitter using seperate encoder unit.

At the robot unit, the RF transciever recieves the digital value which was sent from . The values are decoded and after processing, the respective servor motors are operated. 