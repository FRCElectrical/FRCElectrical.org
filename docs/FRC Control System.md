---
title: FRC Control System
---

# The FRC Control System

## Control system basics: 
- Battery, SB50 and/or 120: Originates all of the power to the robot.
- Main breaker
- Power distribution: Power originates with distribution hub or panel (PDH/PDP/Andymark): do not use the switchable port on PDH for essential components as it has been known to flicker on and off
- Fuses
- Mini Power distribution
- Gyro
- Systemcore
- Radio
- RSL
- Motor/Motor controller
- Encoders: Swerve encoders can be spliced from a single wire into 5 port wago. Soldering is a way that teams have done this. You’ll learn later why soldering is considered bad for an FRC environment, but for now, just understand it is a worse solution than others. A 5 port wago is the most common correct way to accomplish a 4 way splice for encoder wires.  
- Camera
- Terminating resistor


## CAN 
CAN can be wired in two different ways:
- Daisy chained: this is the way that CAN is meant to be wired, and it is the most common way that FRC components are wired. CAN wires originate at the Systemcore in one of the CAN bus ports. The wires then go to each component in order, ending at the terminating resistor. 
- Star topology (DO NOT DO): This is the method used of branching the CAN bus by each individual component. This is used by some teams because in a normal CAN bus, if one component loses a connection, they all do. With a Star topology, each component has its own individual “CAN bus”. This is not recommended at all in modern FRC, as the introduction of SystemCore allows you to split up CAN buses much further than originally. Additionally, a star topology presents many issues as it is NOT AT ALL how CAN is meant to be wired.

Always place resistor at end of each loop (120 OHM resistor in a wago or if terminating at a motor w/board (include why not to use the PDH resistor if using a PDH)
Electrical Components

## Motors:
Intro to motors: Motors are the joints of the robot; they control every moving and rotating component on most modern robots. Thus, wiring them is very important. There are two types of motors, brushed and brushless. In FRC, all that really needs to be known is that brushed motors aren’t used any more. However, outlines of both types will be provided below before the motors most commonly used in FRC are.
- Brushed 
- Brushless

1. Krakens (best pick for quality, talon FX gives integrated motor controller
2. Neo
3. CIMs

### Motor controllers
- Talon FX: Motor controller that is integrated into motors such as Kraken (x60/x44). Talon FX acts as an integrated motor controller meaning that an external controller that is separately wired is not needed. For Kraken X60/X44s, wiring is relatively simple because the controller is integrated in the motor itself. CAN and Power directly stem from the motor and can be connected to their appropriate locations. Power being the Distribution Panel/Hub and CAN into the chain.
- SparkMAX
- Spark Flex
- Thrifty Nova
- Talon FXS
## Gyros:
- Pigeon
- CANandGyro

### Power distribution
- PDH
- PDP

## Systemcore
1. https://docs.wpilib.org/en/latest/docs/software/systemcore-info/systemcore-introduction.html 
2. https://community.firstinspires.org/systemcore-alpha-testing-first-wave 

### Mini power distribution
- Rev MPM
- VRM

## Cameras
- Arducams
- Limelight

## Sensors
- CANRange
- Limit Switch
- Encoders
- Mag Switch
- CANAndColor
- Beam Breaks
