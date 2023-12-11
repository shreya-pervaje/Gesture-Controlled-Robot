The project contains a robot unit and a gesture unit. The hand gestures control the movement of the robot and its clamper.

This file contains two different scripts written on two microcontrollers present on two units: The gesture unit and the robot unit. The gesture unit consists of a glove with a microcontroller and gesture sensors connected to its input port. A 433MHz RSI wireless transceiver module enables the wireless transmission and the HT12E & HT12D encoders and decoders used for the encode/decode process. The robot unit consists of a chassis on which the battery, the servomotors and a microcontroller are mounted together.


# How to run the code
The gesture unit code "Gesture_unit.c" contains the commands to read the gesture from the sensors. The code is written onto a microcontroller placed on a glove with gesture sensors. The RF transmitter sends the encoded message to a receiver.

The robot unit code "Robot_unit.c" contains the instructions for the servo motor to move the robot and a clamper and is written to the microcontroller on the Robot unit. 

# What does the code do
Gesture_unit.c: 
The gestures read from sensors connected to the analog ports of the Atmega 328p microcontroller are processed to cause movement in the robot. The values from the sensors are calibrated to detect the sensor value changes. These changed values are converted to digital data using analog-to-digital conversions with the help of prescalers in the code. The values are further processed and sent to the RF transmitter after being encoded using a separate encoder unit.

Robot_unit.c: 
At the robot unit, the RF receiver receives the encoded message. The decoder provides these values to the code that does the further processing. The logic controls the movement of the robot and its clamper according to the hand gestures given by the user.

The overall working of logic is shown in the following flowchart. 

![image](https://github.com/shreya-pervaje/Gesture-Controlled-Robot/assets/151652737/6d735dd0-5959-4414-82df-00e4a244f3c5)
