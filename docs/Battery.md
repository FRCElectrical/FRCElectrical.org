---
icon: lucide/battery-charging
title: Batteries
---

## FRC Batteries

FRC uses 12-Volt 18 Amp-Hour Sealed Lead Acid (SLA) batteries. These batteries are the Absorbed Glass Mat (AGM) type, which contain fiberglass mats with absorbed battery acid, instead of free-flowing liquid. This reduces the consequences of a spill and results in safer batteries. 

SLA batteries are intended for use in lower current applications, with nominal outputs between 1 to 15 amps and can last many years in these conditions. Under FRC conditions, which average around 50-60 amps continuous through the match, batteries tend to last 1-2 years before becoming unsuitable for matches.

![Battery Examples](/assets/Battery/batteries-combined.png)

!!! danger "Battery Safety"
    While AGM batteries are safer than free-flowing liquid batteries, battery acid is still an extremely strong acid, as well as being highly toxic. If a battery is dropped, cracked, or you see any white powdery residue on it, dispose of the battery safely following your team's battery disposal procedures.

## Battery Components

![Battery Wiring Diagram](/assets/Battery/battery-wired.png){ width="50%", align=left }

1. An Anderson SB-series connector.
+ Thick gauge battery wires.
+ The lug and connectors attaching wires to the battery.
+ The battery itself.

### 1. Anderson SB Connectors
There are two types of Anderson SB connectors permitted for use as FRC battery connectors; the SB50 and SB120. The SB50 is the most common, and is rated for 6AWG wire. By swaging the connector it is possible to use with 4AWG, but switching to an SB120 is recommended in that case. SB50 connectors are used on batteries from FRC spares kits, as well as those that come as part of the rookie kit of parts. SB120 connectors are rated for 6AWG, 4AWG, and 2AWG wire depending on the size of contact purchased.

SB connectors are color coded, and do not interconnect between colors. For the SB50, red is the most common color. For the SB120, blue is the most common color. Using a less common color may prevent borrowing or sharing batteries with other teams.

#### Recommended SB Connectors
| Wire Size | Type | Powerwerx SKU | Link |
| --------- | ---- | ------------- | ---- |
| 6AWG | Red SB50 | SB50-06-RED | [Powerwerx](https://powerwerx.com/anderson-sb-connectors-sb50-50amp) |
| 6AWG | Blue SB120 | SB120-06-BLU | [Powerwerx](https://powerwerx.com/anderson-sb-connectors-sb120-120amp) |
| 4AWG | Blue SB120 | SB120-04-BLU | [Powerwerx](https://powerwerx.com/anderson-sb-connectors-sb120-120amp) |
| 2AWG | Blue SB120 | SB120-02-BLU | [Powerwerx](https://powerwerx.com/anderson-sb-connectors-sb120-120amp) |

### 2. Battery Wires
The most common wire gauge for FRC battery wires is 6AWG. 4AWG and 2AWG are also permitted, and provide slight benefits to conductivity, increasing the amount of usable power for the robot. Using EPDM welding cable is recommended, as it's extremely flexible and cut resistant, [Powerwerx](https://powerwerx.com/welding-cable-epdm) sells this type of cable in 6AWG, 4AWG, and 2AWG gauges.

If you don't want to cut and crimp the wires yourself, AndyMark sells pre-made battery cables in [6AWG](https://andymark.com/products/6-gauge-12-inch-battery-cable?variant=44497405870252) and [4AWG](https://andymark.com/products/4-gauge-battery-cable), as well as configurable [Robot Power Cable Kits](https://andymark.com/products/robot-power-cable-kit-custom-lengths-up-to-36-in) that cover the entire system.

When designing your robot, you want to minimize the battery wire length to the power distribution board as much as possible. This reduces resistance, and allows for more effective power.

!!! warning
    While Copper Clad Aluminum (CCA) wire is allowed, it is not recommended. For the same wire diameter CCA wire has a higher resistance and will waste significantly more power as heat, leading to worse performance and hotter wires.

### 3. Lugs and Connection
FRC battery terminals are designed for use with lugs compatible with #10-32 or M5 screw holes. Lugs must be sized appropriately for the wire gauge being used. Depending on your battery orientation, you may want to use a straight or right angle lug. Once crimped, the lug should be attached to the battery terminal using locking hardware. 

The best option is the Grasshopper nut, which provides an extremely secure connection that resists loosening under vibration. Grasshopper nuts can be purchased from [The Thrifty Bot](https://www.thethriftybot.com/products/grasshopper-nut), or made yourself using this [forming tool](https://cad.onshape.com/documents/fd2d9412535523e7783f88ba/w/d2d16c539f14e2ce19b152b7/e/58dd4fa889f825cfdecfe609). If you cannot use a Grasshopper nut with Nord-Lock washers, a #10-32 screw with washers and a nylock nut is the next best option. 

![Grasshopper Nut](/assets/Battery/grasshopper-nut.png){ width="50%" }

!!! warning
    The hardware that comes with the battery at purchase is usually extremely low quality, and may loosen during matches, leading to a faulty connection and loss of power. It's is highly recommended to replace them with better hardware.

#### Recommended Lugs
| Wire Size | Lug Orientation | FerrulesDirect SKU | Link |
| --------- | --------------- | ------------------ | ---- |
| 6AWG | Straight | SB610 | [FerrulesDirect](https://www.ferrulesdirect.com/products/sb610) |
| 6AWG | Right Angle | SBF610 | [FerrulesDirect](https://www.ferrulesdirect.com/products/sbf610) |
| 4AWG | Straight | SB410 | [FerrulesDirect](https://www.ferrulesdirect.com/products/sb410) |
| 4AWG | Right Angle | SBF410 | [FerrulesDirect](https://www.ferrulesdirect.com/products/sbf410) |
| 2AWG | Straight | SB210 | [FerrulesDirect](https://www.ferrulesdirect.com/products/sb210) |
| 2AWG | Right Angle | SBF210 | [FerrulesDirect](https://www.ferrulesdirect.com/products/sbf210) |

### 4. The Battery
The most commonly used batteries in FRC are the MK Battery ES17-12, the Duracell DURA12-18NB, and the Energizer EN18-12. These can be purchased from FRC vendors, or from most automotive vendors. If purchasing batteries in person, check the date of manufacture. Batteries that have sat on the shelf for a long period of time may have lost some of their total capacity. To understand what specs make a battery legal, please see [R601](https://www.frcmanual.com/2026/robot-construction-rules-(r)#r601-battery-limit-everyone-has-the-same-power).

## Crimping and Assembly
Both the lugs and SB-series connectors need to be correctly crimped with enough force to solidify the stranded wire within the lug. To do this, there are a few crimper options that provide good crimps. The cross section of a correctly crimped wire should look like the left image below, with the strands compressed into each other. The right image shows a poorly crimped wire, which may lead to connection failure and increased resistance.

A good way to check your crimps is the "tug test", where post crimp you pull on the connection to see if it moves on the wire. If any movement occurs, it was not crimped properly.
![Crimped Wires](/assets/Battery/crimps.png)

| Crimper | SKU | Link |
| ------- | --- | ---- |
| 1-8AWG Benchtop Crimper | IWS-0801DTS | [iCrimp](https://www.icrimptools.com/collections/battery-lug-crimping-tool/products/iwiss-iws-0801dt-hex-crimp-bench-mount-battery-cable-crimper-for-8awg-to-1awg-electrical-non-insulated-cable-lugs) |
| 1/0-8AWG Handhend Crimper | HX-50BI | [iCrimp](https://www.icrimptools.com/products/iwiss-battery-cable-lug-crimping-tool-for-heavy-duty-copper-wire-lugs-battery-cable-ends-from-awg-8-1-0-ground-lug-cimper-tool) |
| 4-70mm² Hydraulic Crimper | YQK-70 | [iCrimp](https://www.icrimptools.com/products/yqk?_pos=1&_sid=119e521b0&_ss=r) |

Clips which can be used to ziptie the battery wires to the structure of the battery are heavily recommended, as they reduce the amount of stress on the lug connections, as wellk as on the SB50. You can purchase them from DigiKey, as [Panduit SKU MCMS12-P-C](https://www.digikey.com/en/products/detail/panduit-corp/MCMS12-P-C/1306790).
![Battery Wire Clips](/assets/Battery/battery-clips.png){ width="50%" }

### Battery Assembly Steps
1. Cut both wires to the desired length. Remember that the shorter your battery wires are, the better performance you will get.
+ Strip insulation off the ends to the spec for that connector. For lugs, this is the length of the barrel, with a minimum amount of uninsulated wire sticking out. For SB-series connectors, this is **9/16" (14mm)** for SB50 connectors, and **15/16" (24mm)** for SB120 connectors. While stripping the cable, be careful not to cut any strands. This can reduce current carrying performance.
+ Crimp the lugs and SB-series connectors using the appropriate crimper and die for your wire gauge, as mentioned above. In the case of using a crimper with metric mm² dies, you can use an online tool to [convert AWG to mm²](https://www.rapidtables.com/calc/wire/awg-to-mm.html). <br/> <!-- Adds line break while keeping text inside list number -->
In the images below, on the left you can see an example of flashing, where the die has squeezed some of the metal out of the crimp. In small amounts, like in the image, this is okay, but larger flashing can lead to poor connection quality. <br/> <!-- Adds line break while keeping image inside list number -->
  ![Mild Flashing](/assets/Battery/mild-flashing.jpg){ width="50%" }
+ Use heat shrink tubing to cover the barrel of the lug. Do not cover the flat mating surfaces, and do not apply heat shrink to the SB-series connector.
+ Insert the pins into the SB-series connector housing, and ensure they are fully seated. The bent tip of the contact should be pushed in front of the spring in the connector housing, retaining the contact. 
+ Connect the lugs to the battery terminals using a Grasshopper nut, or #10-32 screw with washers and a nylock nut. Be careful not to over-tighten the connection, as this can damage the battery terminal and cause battery leakage. <br/> <!-- Adds line break while keeping image inside list number -->
  ![Battery Terminal Leak](/assets/Battery/battery-oxidation.JPEG){ width="50%" }
+ Use heatshrink or electrical tape to cover all exposed metal on the battery terminals, and if possible use the clips mentioned in [Crimping and Assembly](#crimping-and-assembly) to provide strain relief for the battery wires.