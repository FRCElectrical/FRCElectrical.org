---
title: FRC Control System
icon: lucide/zap
---

# The FRC Control System

## Control system basics

### Battery
- SB50 and/or 120: Originates all of the power to the robot.
### Main breaker
- todo
!!! warning

    DO NOT use the Optifuse breaker.
### Power distribution 
- Power originates with distribution hub or panel (PDH/PDP/Andymark)
### Fuses
- todo
### Mini Power distribution
- todo
### Sensors
- todo
- Encoders
### SystemCore
- todo
### Radio
- todo
### RSL
- todo
### Motors/Motor controllers
- todo
### Cameras
- todo: also consider co-processor section?
### Terminating resistors
- todo


## CAN 

CAN can be wired in two different ways:

- Daisy chained: this is the way that CAN is meant to be wired, and it is the most common way that FRC components are wired. CAN wires originate at the Systemcore in one of the CAN bus ports. The wires then go to each component in order, ending at the terminating resistor. 

- Star topology: This is the method used of branching the CAN bus by each individual component. This is used by some teams because in a normal CAN bus, if one component loses a connection, they all do. With a Star topology, each component has its own individual “CAN bus”.

!!! warning

    DO NOT use star topology for CAN FD (AKA, SystemCore / CTRE CANivore). Star topology will result in severe signal degradation, intermittent communication dropouts, and high bus error rates during high-speed data phases.

!!! info

    Always place resistor at end of each loop (120 OHM resistor, include why not to use the PDH resistor if using a PDH)

## Electrical Components

### Motors

Intro to motors: Motors are the joints of the robot; they control every moving and rotating component on most modern robots. Thus, wiring them is very important. There are two types of motors, brushed and brushless. In FRC, all that really needs to be known is that brushed motors aren’t used any more. However, outlines of both types will be provided below before the motors most commonly used in FRC are.
- Brushed 
- Brushless

#### WCP Krakens 
- (best pick for quality, talon FX gives integrated motor controller)

##### X60
- X60 is the 60mm diameter Kraken
##### X44 
- X44 is the 44mm diameter Kraken

#### REV NEO
##### NEO 1.2
- todo
##### NEO 2.0
- todo
##### NEO Vortex
- todo

#### CIMs
- CIMs are brushed motors
##### 2.5in CIM
- todo
##### Slim CIM
- todo

#### Small Brushless Motors
- 550 / 775 Class Motors
##### CTRE Minion
- todo
##### Thrifty Nova
- todo


### Motor controllers

#### Talon FX
- Motor controller that is integrated into motors such as Kraken (x60/x44). Talon FX acts as an integrated motor controller meaning that an external controller that is separately wired is not needed. For Kraken X60/X44s, wiring is relatively simple because the controller is integrated in the motor itself. CAN and Power directly stem from the motor and can be connected to their appropriate locations. Power being the Distribution Panel/Hub and CAN into the chain.

#### REV SparkMAX
![Spark MAX](/assets/SPARK_MAX.png)

- Use Andersons to connect the SparkMAX to the motor
- Use Ferrules to connect the SparkMAX to the Power Distribution Solution

!!! warning
    Example Warning
#### REV Spark Flex
- todo
#### Thrifty Nova
- todo
#### CTRE Talon FXS
- todo



### Power distribution

#### REV Power Distribution Hub (PDH)
- todo
#### CTRE Power Distribution Board 2.0 (PDP)
- todo
#### AndyMark Power Distribution (AMPD)
- todo

### Systemcore

1. https://docs.wpilib.org/en/latest/docs/software/systemcore-info/systemcore-introduction.html 
2. https://community.firstinspires.org/systemcore-alpha-testing-first-wave 

### Mini power distribution

#### REV Mini Power Module (MPM)
- todo
#### VRM
- todo

## Cameras

- Arducams
- Limelight

## Sensors

### IMUs / Gyros
#### CTRE Pigeon 2.0
- todo
#### Redux CANandGyro
- Todo

### Encoders
#### CTRE CANCoder
- todo
#### Redux CANAndMag
- todo
#### Thrifty Absolute Magnetic Encoder
- todo

### Distance Sensors
#### CTRE CANrange
- todo
#### Redux CanAndColor
- Both a distance and color sensor

### Other Sensors
#### Limit Switch
- todo
#### Mag Switch
- todo
#### Beam Breaks
- todo
