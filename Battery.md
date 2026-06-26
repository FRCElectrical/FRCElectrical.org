---
icon: lucide/zap
title: Contribution
---

# Batteries
* FRC Batteries are 12V Sealed Lead Acid (SLA) Batteries- the same kind found in your car. 
* In FRC, we try to push our batteries to the limit so that our bot gets the most power possible delivered in the most efficient way. By pushing batteries to their limits, we need to be very careful. This means for one following all of the safety guidelines to a tee, as batteries can quickly become the most unsafe thing on the robot. 

## What to Get
* SLA Batteries come from many vendors. For FRC, we use 3 brands mainly: [Duracell](https://www.batteriesplus.com/product-details/sealed-lead-acid/battery/duracell-ultra/slaa12=18nb?storecode=847&source=google&medium=search&campaign=ecommppc&gad_source=1&gad_campaignid=22449530331&gbraid=0AAAAADgLl5V8SjVLRuUho-ntKgukCfuuM&gclid=CjwKCAjwuuPRBhAnEiwA2Ji8egYnQGYlc_-MwXLNTL3WrZ4Lnflg1MSxvJ7FVTnajWR_du3X8Nq2nhoCPzkQAvD_BwE), [Energizer](https://andymark.com/products/energizer-en18-12v-sla-battery?srsltid=AfmBOooztzZ5x0MIwI7O2a1xBPfYKvO2IUv87yQGBW8DTM_xbGeWM2z1), and [MK](https://andymark.com/products/mk-es17-12-12v-sla-battery-set-of-2?srsltid=AfmBOoqYQC4rZoPfqriHaM3sP9d_8v28mfRGEqA09tlmUgvXY8S4WQ7M). 

## Wires/Connectors for Batteries
* There are two main options for battery wires and battery connectors. We use 4 and 6 AWG wire for batteries and for connectors we use [SB50s](https://powerwerx.com/anderson-sb-connectors-sb50-50amp?srsltid=AfmBOooEGI9cCmnGoLNoHptg3VvKkSyAbujIvzm3Ka8k7bPd4rj6Me6m) and [SB120s](https://powerwerx.com/anderson-sb-connectors-sb120-120amp). 
* You will usually pair up 6 AWG with SB50s and 4 AWG with SB120s, but people have gotten away with fitting 4 AWG wires into SB50s. This is not recommended, because that is not what the SB50 is rated for and makes things needlessly difficult. 
* 4 AWG with SB120 connectors is recommended, as this provides slightly more efficient current draw when compared to 6 AWG and SB50s.

## Battery Assembly
* The two ways that battery lugs can be connected are by using 2 Nordlock Washers or by using a [Grasshopper Nut](https://www.thethriftybot.com/products/grasshopper-nut) with 2 Nordlock Washers. Both methods will be used in tandem with a 10-32 bolt and nut, with heatshrink placed over top.
  * Grasshopper Nut: It provides a mechanical interlock between the battery terminals. It allows for an incredibly secure connection. To create this from scratch, create the sheet metal part through a machining service or in house, then insert the PEM nuts and bend the part using a 3d printed jig with this [CAD](https://cad.onshape.com/documents/fd2d9412535523e7783f88ba/w/d2d16c539f14e2ce19b152b7/e/58dd4fa889f825cfdecfe609?configuration=List_cS05PEshcmecMn%3DDefault&renderMode=0&uiState=64fb8ab3650a1276b653f858) provided for by TTB.
  * Nordlock Washers: Basically a serrated washer. When tightened, the serrations embed into the surfaces, which creates a wedge effect, so as to maintain preload and prevent loosening.
  * Warning: NEVER use the built in stuff. Sure, it works but it creates a loose poor strength connection. In fact NASA has proven lock washers useless for preventing loosening during vibrations as found on page 9 of their [study](https://ntrs.nasa.gov/api/citations/19900009424/downloads/19900009424.pdf) (page 13 of the actual PDF).
* The Lug will be connected to the wire the same as the connector terminal is done so. Read the next section for information.

### The Connector, Lug, and Wire
* The [Lug](https://newwiremarine.com/product/battery-lug/) (generic product link attached) can be from practically anywhere. The only requirements it needs to have is that it is rated for 10-32 hole sizing and whatever wire gauge you choose to use. The terminal should be whatever comes with the connector.
* The Battery crimp is extremely important. The [iCrimp Crimper](https://www.icrimptools.com/products/iwiss-hx-50b-cross-border-crimping-pliers-wiring-pliers-bare-terminal-pliers-yo-copper-aluminum-cable-crimping-pliers-6-50mm2?variant=42722324611233&country=US&currency=USD&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic&cmp_id=22605560113&adg_id=&kwd=&device=c&utm_term=&utm_campaign=B2C+-+New+and+Existing+Customers+-+Perfomance+Max+-+Sale&utm_source=adwords&utm_medium=ppc&hsa_acc=7336915727&hsa_cam=22605560113&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad_source=1&gad_campaignid=22595559102&gbraid=0AAAAAD3ralOpgLD6W26ZBrohaE5P-MYUa&gclid=CjwKCAjwuuPRBhAnEiwA2Ji8evZTr5803jmrVq-7P3k5naQsNKxGMivJepo2QYzHoe-6stGGP_HpphoCMsgQAvD_BwE) is recommended
* Step 1: Strip your wire to the length of the terminal or the lug. For exact measurements, check the documentation or compare the length to the terminal/lug with your eyeball. 
  * The wires you will be using are high gauge and regular strippers won't work on them. Therefore, you should use a pair of flush cutters and be careful to not nick any strands (if this is done, cut off the end and try again). 
  * Fingers may also be used to peel back the insulation with risk to your skin.
* Step 2 (FOR LUGS ONLY): Place the heatshrink on for the lugs. This should be done now rather than later as lugs and terminals may be bulky.
* Step 3: Crimp the connector. Usually your crimper will have a hexagonal die and will sometimes have the millimeter number on it. 
  * For 4 AWG use the 25 setting, as 25mm^2 is equal to 4 AWG. 
  * For 6 AWG use the 16 setting with the same logic. 2 crimps for each terminal/lug is recommended for optimal grip onto the wire. 
  * This crimp takes a lot of force and may be hard for some so assistance can always be asked for.
* Step 4 (FOR LUGS): For lugs, perform the steps described in [Battery Assembly](link), and then, being careful to not allow any metal (including the metal already on the battery) to be exposed, move forward and heat up the heat shrink.
* Step 4 (FOR CONNECTORS): once both wires are done, place them into the connector, with red as positive and black as negative. The hook should go over the metal bit at the end and a click should be heard. To undo, use a flathead screwdriver to pry the hook over the metal bit.

## Maintaining Your Battery
What you need to do to make sure your battery remains competitive!

### Charging
* The [AndyMark NOCO Chargers](https://andymark.com/products/frc-battery-charger?srsltid=AfmBOoqwFmhqzrKGyEGLmltHpnLuQzWZ-Z9BuJ_KRqhnXo1Yxh9rbe2H) are heavily recommended. These come with FRC connectors and are very good chargers.

### Checks
* [CTRE’s Battery Beak](https://store.ctr-electronics.com/products/battery-beak?srsltid=AfmBOorYtOxTG61A61ysMHFyl9BZpIvloOV9aF1eHups2mpyPCVNX0zS) is a tool for quick battery checks during competition: it’ll let you know whether your battery is good or not with a simple plug in to your battery. If you are using a SB120 get the [CTRE Adapter](https://store.ctr-electronics.com/products/sb120-to-sb50-adapter-cable?pr_prod_strat=e5_desc&pr_rec_id=a7835906b&pr_rec_pid=8329799860397&pr_ref_pid=7863765467309&pr_seq=uniform) or for a cheaper cost, create the adapter yourself with an SB50 set, SB120 set and 6 AWG wires.
  * For matches:
    * Ideally under 15 milliohms internal resistance.
    * Ideally at least 120% at the top left. 130%+ is incredibly ideal.
  * For testing:
    * Under 20 milliohms. If your battery is over 20 milliohms, do not use it at all on your robot, as it will demonstrate poor performance.

### Overall Health Tests
* For basic health tests, the battery beak with internal resistance can be used. However, for capacity tests and overall health tests a dedicated tool should be used.
* Cheaper Option: Use a car battery checker. This will provide for a great overall health test. Purchase an [analyzer](https://www.amazon.com/dp/B07Z67MMGC) and crimp either an SB120 or 50 to it.
* If you want to do an actual capacity test and have the money, get a [CBA](https://andymark.com/products/computerized-battery-analyzer?srsltid=AfmBOooGLWRoXcV3QuroNVp4GET2FpbFHrLxtE4HO8NeLZByQJkEZoeH). 
  * It graphically displays and charts the voltage versus time under a constant current load. Graphs can be displayed, saved and printed, and axis parameters can be changed at any time. 
  * Multiple test graphs of the same battery, or multiple batteries, may be compared or overlaid.

### Best Practices
* Always write down when the battery is first used: You can use the AndyMark stickers that come with the kit or just use a sharpie and some tape. Label month and year.
* Have a set circulation of batteries at competition. Regulate based on the performance of each battery.





