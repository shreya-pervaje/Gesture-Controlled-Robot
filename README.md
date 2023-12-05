The project contains robot unit and gesture unit. The gestures are used to control the movement of the robot and its clamper.

This file contains two different scripts to be burned on two different units: Gesture unit and Robot unit. 


# How to run the code
The gesture unit code "Gesture_unit.c" code containing the commands to read the gesture from the sensors is burned to the microcontroller, which is placed on the gloves along with the gesture sensors and RF transmitter.

The robot unit code "Robot_unit.c" code containing the instructions to the servo motor to move the robot and the clamper is burned to the microcontroller on the Robot unit which is build with chasis, servo motors and RF reciever. 

# What does the code do
Gesture_unit.c: The gestures are read from sensors connected to the analog ports of Atmega 328p controller. The values from the sensors are caliberated to read the sensor value changes and are converted to the digital values using Analog to digital conversions with the help of prescalers. The values are further processed and are sent to RF transmitter using separate encoder unit.

Robot_unit.c: At the robot unit, the code receives the values from decoder, which performed the received the values from RF receiver. The logic controls the movement of the robot and its clamper in the desired way.

The overall working of logic is shown in the following flowchart. 
![image](https://github.com/shreya-pervaje/Gesture-Controlled-Robot/assets/151652737/6d735dd0-5959-4414-82df-00e4a244f3c5)
