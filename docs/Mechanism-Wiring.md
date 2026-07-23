---
icon: lucide/cable
title: Mechanism Wiring
---

# Specific Mechanism Wiring

## Turret
Turrets rotate and electronics on whatever mechanism is on said turret need to get power. The wires that go to them can break, however. Thus, we need methods to effectively transfer power/CAN. Two main ways are used to do this, both involving a BIGUS chain.

There are two suggested methods to wiring a Turret
<video controls width="50%" preload="metadata">
  <source src="assets/Mechanisms/Turret/PXL_20260220_0440071372.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<div style="text-align: left; margin: 20px 0;">
  <iframe 
    width="315" 
    height="560" 
    src="https://www.youtube.com/embed/g33nFoGUTaQ" 
    title="YouTube Short" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    allowfullscreen
    style="border-radius: 12px; box-shadow: 0 4px 10px rgba(0,0,0,0.1);">
  </iframe>
</div>


## Elevator
The elevator carriage should be wired with a [BIGUS chain](https://www.igus.com/cable-carriers). This chain should be included in CAD with mounting points provided on elevator crossbeams. Ensure that the motion of any other subsystem (such as an end effector) does not interfere with the possible gravitational motion of the energy chain when moving linearly.

254 has some tips on how to effectively manage a e-chain [here](https://www.chiefdelphi.com/t/most-common-issues-seen-on-robots-this-year/466119/69?u=jimmyy)

=== "3506 YETI Robotics"
    ![YETI-2024](/assets/Mechanisms/Elevator/Kitty2024PracticeField-removebg-preview.png){ width="50%" }
=== "Second Example"
    ![Second](/assets/Mechanisms/Elevator/47U4BdC-removebg-preview.png){ width="50%" }


## Linear Intake
* Linear slides work very similar to Elevators. Both move in a straight motion and often show the same wiring solution. 
* You can wire a linear slide through two main reliable methods
  * Nylon Wire Loom
  * Energy Chain
* When using an Energy Chain, ensure that your energy chain has the hard end towards the edge of the intake. This ensures that the Energy chain does not compress and enter farther into the hopper space. You can also use hard stops using 3d print or other material
* When using a wire loom, ensure that the ends meet at the beginning and end of intake. Make sure that the wire loom does not bend upwards or flail around the hopper space (typically means you would need a hard stop).

=== "3506 YETI Robotics"
    ![YETI-2026](/assets/Mechanisms/Linear-Intake/DePb2t1-removebg-preview.png){ width="50%" }

## Drivetrains
- All of the electronics placement should be done in CAD. The electrical team should work with CAD to ascertain these locations. They can be fastened within either mounting holes, VHB, or Zipties. Grommet holes and grommets should be put into tubes so that wires can easily pass through without risk of damage.

=== "254 2017"
    ![254-2017](/assets/Mechanisms/Drivetrain/254-2017.jpeg){ width="50%" }
=== "254 Example"
    ![254-example1](/assets/Mechanisms/Drivetrain/254-example.jpegg){ width="50%" }
=== "2724 Avalanche: 2026 Brainpan"
    ![1538-example](/assets/Mechanisms/Drivetrain/1538-example.jpeg){ width="50%" }

### Brain Pans
- Brainpans (electronics underneath the bellypan of the robot) can be used to minimize the space that electronics take up. This can be for games where maximizing space on the robot is everything (i.e. Rebuilt™)
- In usage, ensure that electronics are protected and have easy access

=== "9496 LYNK: 2026 Brainpan"
    ![9496-2026-Brainpan](/assets/Mechanisms/Brainpan/9496-2026-Brainpan.jpeg){ width="50%" }
    ![9496-2026-Brainpan-1](/assets/Mechanisms/Brainpan/9496-2026-Brainpan-2.jpeg){ width="50%" }
=== "2724 Avalanche: 2026 Brainpan"
    ![2724-2026-Brainpan](/assets/Mechanisms/Brainpan/2724-2026-Brainpan.jpeg){ width="50%" }
