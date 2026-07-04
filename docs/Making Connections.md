---
icon: lucide/zap
title: Contribution
---

# Making Connections

This page covers everything needed for you to make successful connections in the FRC Control System

## Crimping Connectors
* Molex (explain to cut off Dupont): This is the single best connector for CAN and low AWG power wire. It’s easy to crimp, low profile, shrouded, and pin and socket. Two-pin Molex is the standard for integration into SystemCore and Adapter boards for Krakens. Using the TPA is also heavily recommended, as it raises the terminal retention from 17.5 N to 50+N, as seen in the poster. 
  * [Crimping Molex (Video)](https://www.youtube.com/watch?v=khB2-0bkj9Q)
  * [Crimping Molex (Guide)](https://www.molex.com/content/dam/molex/molex-dot-com/en_us/pdf/general/Final_Crimp_Poster_FIRST.pdf?inline)
* Anderson: For higher AWG power wire, Anderson is the best connector. The TRIcrimp is recommended for crimping, as well as the tin-plated connectors.
  * [Crimping Anderson (Video)](https://www.youtube.com/watch?v=NwgLyCA1N-4)
* Powerpole adapter boards
  * As mentioned previously, these are boards for Krakens that convert the ring terminal outputs to Anderson and Molex.  
* Ferrules: Used for wires that connect to the ports of components like the RIO/SYSTEMCORE or PDH as well as for connections that involve linear WAGOs.


## Solder
* Solder connections, as opposed to crimped connections, are sometimes weaker and less reliable. 
!!! warning
  * They are HEAVILY discouraged for teams, and especially newer teams. The reason that teams usually go this route is that they’re seen as equivalent to a continuous run. In fact, soldering is a failure point on the bot, and like connectors, it needs to be properly strain relieved. 
* Soldering is relatively easy once it's learned, but there is a learning curve, as well as more room for error than crimped connectors. Additionally, in an FRC environment it’s fast paced. 
* If something breaks or needs to be replaced it’s extremely challenging.

## Lineman's Splice
* The Lineman’s Splice also known as the [NASA Splice](https://m.youtube.com/watch?v=O-ymw7d_nYo) is probably the highest strength solder joint, and also the one with the profile best fit for heatshrink.
  * Solder sleeves (explain why not to use them: low-melt solder, which is usually low quality, and doesn't flow well. It's just as easy as normal solder splices to get wrong if you don't apply enough heat for long enough.)
* 221 Inline WAGOs & y/g WAGOs
  * Solder connections are not advised as they are fragile and do not typically stand through much strain
  * Crimp connections are recommended