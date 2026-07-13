---
icon: lucide/zap
title: FRC Control System
---

# FRC Control System

## Control System Basics

* Battery supplies Power to the Robot
* Power originates with a distribution hub or panel (PDH/PDP/Andymark) (include not to use the switchable port on PDH for essential components, as it has been known to flicker on and off)
* Swerve encoders can be spliced from a single wire.
  * Soldering is a way that teams have spliced. You’ll learn later why soldering is considered bad for an FRC environment, but for now, just understand it is a worse solution than others. 
  * A 5-port [Wago](https://www.amazon.com/LEPEVNEY-Electrical-Connectors-Retardant-Connector/dp/B0GCJGNR1R/ref=sr_1_4?crid=3S5XVPL2BYERF&dib=eyJ2IjoiMSJ9.fnqoyr8S4BoE6gGHz4zoKNKmHKklMrr4b2weTcpcWDTtgCFb9RqDgBQ5F-tbMFAbu-gasv3x3za6PIa3aqW2dUvf2vMRlnPKnQA48KHO2SYTRiV69c_SfiG7Uk7fiULECS2MLTP-yaaymRvp14ij9Mud3-jhJY4C9Ki-CUEiCTAhYIK6Oak4YNHcirDnV_LF4RVtLIb8UO6KggrtqmTMvYdDPQzeTNgsVz_f8BBDDcQ.zFwnjvta4aXVr957XsFxWN2hmtDJTrVbEffRnxRYKV0&dib_tag=se&keywords=Wago%2B2%2BPort%2B(10)%2B3%2BPort%2B(10)%2B5%2BPort%2B(4)%2BLever-Nut%2BAssortment%2BPack%2BConductor%2BCompact%2BConnector%2BTerminal%2BBlock%2BWire%2BPush%2BCable%2BConnector%2B12-28%2BAWG%2C%2B32A%3A%2BAutomotiveor%2BCompact%2BConnector%2BTerminal%2BBlock%2BWire%2BPush%2BCable%2BConnector%2B12-28%2BAWG%2C%2B32A%3A%2BAutomotive&nsdOptOutParam=true&qid=1780958682&sprefix=wago%2B2%2Bport%2B10%2B3%2Bport%2B10%2B5%2Bport%2B4%2Blever-nut%2Bassortment%2Bpack%2Bconductor%2Bcompact%2Bconnector%2Bterminal%2Bblock%2Bwire%2Bpush%2Bcable%2Bconnector%2B12-28%2Bawg%2C%2B32a%2Bautomotiveor%2Bcompact%2Bconnector%2Bterminal%2Bblock%2Bwire%2Bpush%2Bcable%2Bconnector%2B12-28%2Bawg%2C%2B32a%2Bautomotive%2Caps%2C183&sr=8-4&th=1) is the most common correct way to accomplish a 4-way splice for encoder wires. 

## CAN
* Controller Area Network
* CAN can be wired in two different ways:
  * Daisy-chained: this is the way that CAN is meant to be wired, and it is the most common way that FRC components are wired. CAN wires originate at the Systemcore in one of the CAN bus ports. The wires then go to each component in order, ending at the terminating resistor. (Add diagram). One full loop, as mentioned previously, is called a CAN bus.
  * Star topology (DO NOT DO): This is the method used to branch the CAN bus by each individual component. This is used by some teams because in a normal CAN bus, if one component loses a connection, they all do. With a Star topology, each component has its own individual “CAN bus”. This is not recommended at all in modern FRC, as the introduction of SystemCore allows you to split up CAN buses much further than originally. Additionally, a star topology presents many issues as it is NOT AT ALL how CAN is meant to be wired.
  * Always place the resistor at the end of each loop. This will be a 120 OHM resistor in a WAGO, or if terminating at a motor with a powerpole adapter board, the Weidmuller connectors may be used.

## Specific Electrical Components
### Motors
* Intro to motors: Motors are the joints of the robot; they control every moving and rotating component on most modern robots. Thus, wiring them is very important. There are two types of motors, brushed and brushless. In FRC, all that really needs to be known is that brushed motors aren’t usually used anymore. However, these types of motor can be used in specific applications as well as being offered in the KOP. Outlines of both types will be provided below before the motors most commonly used in FRC are discussed.
  * Brushed: Brushed motors have 4 components: The stator, rotor, commutator, and brushes. In this diagram, the rotor can be thought of as the shaft and rotor coils. They are attached to the commutator. The way it works is this: The stator magnets are permanent, and when electrons are passed from the brushes to the commutator to the rotor coils, it produces a magnetic field opposing the one created by the stator magnets’ fields. However, the magnets would usually stop rotating when the fields are in alignment. How does this get prevented? The commutator uses a specific pattern of metal to make it so that the field always opposes that of the stator magnets, therefore causing rotation. Brushed motors are most commonly used in cheaper appliances.
  * Brushless: Brushless motors are like brushed motors in many ways. They can have an internal or external rotor (the diagram has an internal rotor). What you may notice about the motor is that it has no brushes (duh). How then does it create opposite polarities? This is through an electronic circuit that detects how much the motor rotates. This makes for less contact throughout the system and a more precise transmission of power, which is why brushless motors are used throughout the world and especially in FRC. 
* Common FRC Motors
  * Krakens (Best Pick for Quality): Krakens are arguably the most powerful motor in FRC. There are two types of Krakens- [X60](https://store.ctr-electronics.com/products/kraken-x60?srsltid=AfmBOoolHLgDms10sPZ2hFQxVZrCqbklUjTi9QQvaCkxARJxz1uOZd8N) and [X44](https://store.ctr-electronics.com/products/kraken-x44?srsltid=AfmBOopKr-9t43Uap2jITNGqDDsnkg3THzY--EEx-VA4rGnkshChu-4a) (For 60 mm and 44 mm Outer Diameter, respectively). These motors have built-in motor controllers, called TalonFX, which will be discussed in more detail later. They have two screws for cooling ports on the side that can be removed and covered with electrical tape. For Kraken wiring, there are two ways to go about it, but for both, the [CTRE Torque Wrench](https://store.ctr-electronics.com/products/pre-set-torque-wrench?srsltid=AfmBOooLYptNM7_Vcb-sw1QYtiG6x_efJdQC7caX8DyuCrGtbxJBxO7_) is a tool that makes the application much better and removes hesitancy due to fear of overtightening bolts.
    * You can use the built-in ring terminals. The Kraken comes with them, and with the torque wrench, they’re easy to install. The wiring guide is on the [WCP website](https://docs.wcproducts.com/welcome/electronics/kraken-x60/kraken-x60-+-talonfx/overview-and-features/wiring-and-modularity). This may require extra splicing for longer wire runs, but overall, they are a fine solution.
    * WCP Powerpole Adapter Boards. This replaces the ring terminals with common FRC connectors: Anderson Powerpole connectors and Molex SL connectors, which will be taught later. One extremely important thing to note is that the screws for these are NOT able to be used for ring terminals. That can severely damage the controller and also cause CAN bus issues. These allow for a continuous run and easy removal of wires, no matter what length wire run is necessary. The non-flipped X60’s also allow for termination using their top Weidmuller connectors as a hub for a 120 Ohm resistor. [X60 Board](https://wcproducts.com/products/wcp-1380), [Flipped X60 Board](https://wcproducts.com/products/wcp-1903?pr_prod_strat=e5_desc&pr_rec_id=337093772&pr_rec_pid=9040434102484&pr_ref_pid=7989871542484&pr_seq=uniform), [X44 Flipped Board](https://wcproducts.com/products/wcp-1904?pr_prod_strat=jac&pr_rec_id=06f290df0&pr_rec_pid=9040435544276&pr_ref_pid=9040434102484&pr_seq=uniform)
  * NEO (NEO Vortex and NEO 2.0 best picks for price)
      * There are 4 kinds of NEO motors. The [NEO 1.1](https://www.revrobotics.com/rev-21-1650/), [NEO 2.0](https://www.revrobotics.com/rev-21-1653/), [NEO 550](https://www.revrobotics.com/rev-21-1651/), and [NEO Vortex](https://www.revrobotics.com/rev-21-1652/). All of them are controlled the same way, using an external Motor controller. These, unlike the TalonFX's, aren't built in, so a separate space is needed to mount them. 
  * CIMs
      * [CIM Motors](https://andymark.com/products/2-5-in-cim-motor?srsltid=AfmBOorBBClaISFHUpTn6bFgXE1w_2Pfd6TXEb68cYwynubycuwPgYn_) are the only brushed motors seen on this list. They are the motors FIRST uses on their fields and the motors that come with the kitbot. Similar to NEOs, they are controlled with External motor controllers.

### Motor Controllers
These are the devices that control the motors and help direct power and signals to each mechanism.

=== "Talon FX"

    * This is the controller that is integrated into the Kraken’s (both X60 and X44). Talon FX acts as an integrated motor controller, meaning that an external controller that is separately wired is not needed.
    * For Kraken X60/X44s, wiring is relatively simple because the controller is integrated in the motor itself. CAN and power directly stem from the motor and can be connected to their appropriate locations.

=== "SparkMAX"

    * [SparkMAX](https://www.revrobotics.com/rev-11-2158/) is often considered the best motor controller for price.
    * This is a controller optimized for the NEO brand and works for brushed and brushless motors.

=== "Spark Flex"

    * [Spark Flex](https://www.revrobotics.com/rev-11-2159/) is a motor controller made for integration with the NEO Vortex.

=== "TTB's Nova"

    * [TTB's Nova](https://www.thethriftybot.com/products/thrifty-nova) is Thrifty Bot’s motor controller option.

=== "Talon FXS"

    * [Talon FXS](https://store.ctr-electronics.com/products/talon-fxs?srsltid=AfmBOoqrDtivYz01ZhMZN83ueCLV9vtFR7v5zd-r1RJh8Oi5vd6bPA7f) is optimized for CTRE’s Minion motor and supports CAN FD capabilities.

### Gyroscopes
These allow for the positional accuracy of your robot, as shown on logs. This is important for the autonomous period of your robot in the match, as well as automatic positioning.

=== "Pigeon 2.0"

    * [Pigeon 2.0](https://store.ctr-electronics.com/products/pigeon-2?srsltid=AfmBOopKkbE8euQjLvXkKVGa2Yv38bQL54rZIp9qeEz6EtwOsxAoNflI) is often considered the best quality option.
    * CTRE’s gyroscope.

=== "CANandGyro"

    * [CANandGyro](https://shop.reduxrobotics.com/products/boron-canandgyro) is a strong price-focused choice.
    * Redux’s gyroscope.

### Power Distribution
Power distribution boards are how power gets around the robot. They can range from complex circuits to simple copper blocks.

=== "PDH"

    * [PDH](https://www.revrobotics.com/rev-11-1850/) is often considered the best quality option for teams that want a robust and modern distribution board.

=== "PDP"

    * [PDP](https://store.ctr-electronics.com/products/power-distribution-panel?srsltid=AfmBOopoSK1Di0TRjaJsVxDZllI60QdiBW1o38FV_IUtqpSCJSKLoa_b) is a strong budget-friendly choice for teams looking for a reliable lower-cost option.

=== "AndyMark Power Distribution"

    * [AndyMark Power Distribution](https://andymark.com/products/ampd-andymark-power-distribution?srsltid=AfmBOopdgvZPfxxJGLdfxQgPt86E32aLuTbFDHg2agWxzwtasnfxGd3m) is another common choice that works well for many FRC teams.

### Fuses and Breakers
* Breakers and fuses are what gets stuck into the power distribution boards so that your precious and expensive electronics don’t break from a potential voltage overload. They are meant to break the electrical connection after too much electricity is supplied, and thereby saving electronics from undergoing that hit. Fuses are sacrificial and always a one time use while breakers are able to be reused in cases, though they can be popped and be rendered unusable.
* Some components will list what breaker should be used on their website but as a general rule of thumb:
  * 10-12 AWG Wire = 40A Breaker
  * 13-16 AWG Wire = 30A Breaker
  * 16-18 AWG Wire = 20A Breaker
  * 22 AWG Wire = 10A Breaker
* [AndyMark Breakers](https://andymark.com/collections/fuses-breakers-distribution/products/snap-action-breakers) are the best choice.

### Main Breaker
* The main breaker is varied in form and is a crucial part of the robot. It’s basically your robot’s on/off switch. It is required to exist and be accessible on every robot. 
* Warning: DO NOT GET OR USE OPTIFUSE BREAKERS. They are prone to failures and pop easier than almost any other kind.
  * Red Levered Breaker (Imperial):
    * This breaker takes a ¼-28 nut.
  * [Yellow Levered Breaker](https://store.ctr-electronics.com/products/120-amp-breaker?srsltid=AfmBOor-v21BDH5-92BFtIYnJAys5dAb1JL0s9RLTLTgBj7XD2WAT5Jv) (Metric):
    * This breaker takes an M6 nut.

### RSL (Robot Signal Light)
* The RSL is crucial to safety on the robot. It turns on when the robot is powered on and blinks when the robot is enabled.
* Wiring the RSL is relatively simple: Make sure the black wire strand from your two strand wire, or ground is in the middle port labeled N, join the two outer ports with a small piece of red wire, and then in the terminal labeled Lb, place the red wire strand from your two strand wire. For easy replaceability, get the [RSL Lever Lock Hub](https://www.digikey.com/en/products/detail/phoenix-contact/1110582/15211615). In both cases, use a small flathead screwdriver for either all wiring or placing the hub in.

### Systemcore
* [WPI Lib Introduction](https://docs.wpilib.org/en/latest/docs/software/systemcore-info/systemcore-introduction.html)
* [Alpha Testing](https://community.firstinspires.org/systemcore-alpha-testing-first-wave)

### Smaller Power Distribution
These are like the power distribution boards, but they are used for electronics that may need smaller voltage. They would be used when you don’t have enough spots on your main distribution board.

=== "REV Mini Power Module"

    * [REV Mini Power Module](https://www.revrobotics.com/rev-11-1956/) is commonly used to provide regulated power to smaller electronics and sensors.

=== "Voltage Regulator Module"

    * [Voltage Regulator Module](https://store.ctr-electronics.com/products/voltage-regulator-module?srsltid=AfmBOoqSvxCWOi-S_hmZN64-mYdpfNRXR3D-_3f4hC0ErgdFZawhhgSz) is used when a stable lower voltage supply is needed for supporting electronics.

### Cameras
These are for vision processing. They’re important in both autonomous and tele-operated periods of your robot.

=== "Arducam"

    * A compact camera option commonly used for custom vision setups.
    * Good for teams looking for flexibility and a lower-cost entry point.

=== "LumaP1"

    * [LumaP1](https://luma.vision/products/p1) is a strong option for teams wanting a modern camera with solid image quality.

=== "ThriftyCam"

    * [ThriftyCam](https://www.thethriftybot.com/products/thriftycam) is a budget-friendly choice for teams looking to keep costs down.

=== "Limelight"

    * [Limelight](https://limelightvision.io/products/limelight-4) is a popular quality-oriented choice for FRC vision systems.

### Sensors
* CANRange: Sensor that uses proximity to automate. Can be used in intakes or passthroughs to automate movement or running of other components (motors, etc)
* Limit Switch: A switch that is typically wired to the Digital Input/Output (DIO) of the control hub. Used to track the range of a mechanism. The sensor contains a physical material, such as a lever, that is typically over an input (like a button). From there, it can track when the button is pressed. This can be used as a hard limit to mechanism movement such as for elevator or pivoting mechanisms. 
* Mag Switch: Mag switches are sensors that detect the presence of a magnet. Typically used to track distance, this sensor is usually used to hard-stops on mechanism movements.
* CANandColor: Sensor that is used to track proximity and color. Can be used in games that have two game pieces of different colors (such as 2025 Reefscape™)  
* Beam Breaks: Sensor that includes an emitter and receiver. When an object passes through the emitter, a signal is sent to the receiver and this can be used to track the movement of a gamepiece within the robot. Automation can be used in pivoting mechanisms for movement.
* Absolute Encoders: These allow for the rotational accuracy of shafts. This is important for swerve drive accuracy rotationally as well as other precise mechanisms.
  * [CTRE](https://store.ctr-electronics.com/products/cancoder?srsltid=AfmBOopMkyo06dBAH539RzxGtOrRWVFucKvbhMIicJZMIfOLGcY7CCxZ) - Quality Pick
  * [TTB Magnetic Encoder](https://www.thethriftybot.com/products/thrifty-absolute-magnetic-encoder) - Price Pick

### Robot Radio 2.0
* VividHosting’s Robot Radio 2.0 (no link yet) is what gets the signal from the driver station to relay information to the robot to make it do all the fun things robots do. Placement of this is especially important and should be done with care. 
  * The radio should be mounted against a metal tube or plate.
    * Heat can build up inside the radio. By mounting the radio against a metal surface, you can conduct heat away, allowing it to disperse.
  * Do not block the visibility of the status LEDs.
  * The radio should not be fully enclosed by a case or mounting solution.
    * This traps heat in the radio and can cause the radio to overheat.
  * The radio should be easily removable, as it is programmed for each competition.
    * Zipties are a great way to mount your radios.
  * Tip: When Radio is placed in a specific location with little bearing on where it is placed, such as on pocketed plates, Outline it with a sharpie.


