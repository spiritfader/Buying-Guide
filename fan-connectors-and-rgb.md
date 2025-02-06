---
title: Fan Connectors & RGB
layout: home
nav_order: 1
has_toc: true
permalink: /fan-connectors-and-rgb
---

# Fan and RGB wiring guide
Understanding PC fan wiring and RGB connections is essential for anyone building or maintaining a computer. Fans are critical for cooling components, while RGB lighting allows for customization of your system’s appearance. However, the variety of connectors and wiring configurations can be confusing for beginners.

This guide provides a straightforward explanation of the different types of fan and RGB connectors, their functions, and how to properly connect them to your motherboard or controller. By the end, you’ll have a clear understanding of how to set up and manage your PC’s cooling and lighting systems effectively.

## Fans
### Essentials
Case fans in computers usually operate at 12V. At the most basic level, they require a positive and a negative connection to function. Simply connecting them to a 12V power source will make them spin at full speed.

However, this isn’t ideal for personal computers, where noise levels matter. To address this, computer motherboards control fan speed using two main methods: **voltage regulation** and **pulse-width modulation** (PWM). 

With **voltage regulation** the motherboard will output a voltage below 12V to spin the fan at a lower rate. 

Using **pulse-width modulation** requires a 3rd connection to supply the fan with a 5V square wave signal. This signal's duty cycle percentage will determine the fan's speed. This method essentially cuts motor power off many times per second (25,000 times to be precise!)

![square wave duty cycle example](https://i.imgur.com/G2VhseE.png) <!--image without timeframe: https://i.imgur.com/TAV8hpr.png-->

Lastly, many fans also have an additional tachometer connection. The fan sends a pulse through the tachometer lead twice per rotation. It's goal is to tell the system how fast the fan is spinning for more precise speed control. 
### Connectors

Fans come in all shapes and sizes, but so do their connectors. These few are the most common:
#### 3 pin connector
The 3 pin connector has been widely used for years. It has 3 connections: negative and positive for **voltage regulation** and a tachometer readout. 

connecting a 4pin connector to a 3pin header is possible, given it isn't blocked by a neighbouring component/connector.


![3 pin connector pinout](https://i.imgur.com/TzcMQ8i.png) 
<br><sup>colours might not match*</sup>


#### 4 pin connector
The 4 pin looks similar to it's predecessor put has an extra pin for PWM control, this is a more modern approach to speed regulation.

connecting a 3pin connector to a 4pin header is possible, voltage control will be needed for speed control.

![4 pin connector pinout](https://i.imgur.com/XAUrjZM.png)
<br><sup>colours might not match*</sup>



#### Peripheral connectors
4pin Molex can frequently be found on cheap cases and case fans, they connect straight to your power supply and thus don't allow for any speed control. This applies to any direct connection to a power supply (E.g. SATA power).
![4 pin Molex pinout](https://i.imgur.com/sMkmC6o.png)
<br><sup>colours might not match*</sup>


#### proprietary connectors
As times have evolved many brands have come out with their own proprietary system for fans and RGB, there are too many to list them all. 

brands notorious for proprietary fan/RGB connectors include: Lian Li, Corsair and NZXT.

![proprietary connectors](https://i.imgur.com/ZKLg0CA.png)


### Splitters, Hubs & controllers
What happens if you have more fans than fan headers? Don't worry, there's always a solution!

#### daisy chain connectors
Some fans will come with an extra female connector chained to their main connector.
Daisy chain connectors will be missing the tachometer pin, this is normal as you can only have one tachometer readout/header.

**Attention:** *A single fan header can only supply a limited amount of current, connecting too many fans to a singular header can cause irreversible damage to your components. Consult your motherboard manual for a max current rating of the header. The power draw of a fan depends on the model, check the back of the fan for a power rating.*
![daisy chain 4 pin PWM](https://i.imgur.com/qfxLnnR.png)
#### Splitters
A splitter is a cable that splits one connector into multiple. This method works with no matter the speed control method, even if there isn't any. 

Only one of the splitter's connectors will have a tachometer pin if applicable.

**Attention:** *A single fan header can only supply a limited amount of current, connecting too many fans to a singular header can cause irreversible damage to your components. Consult your motherboard manual for a max current rating of the header. The power draw of a fan depends on the model, check the back of the fan for a power rating.*
![examples of splitters](https://i.imgur.com/NlnHwV2.png)

#### Hubs
There's many types of fan hubs but most commonly they use the 4 pin PWM fan header.
These hubs replicate the PWM signal across all fans connected to the hub. They also have a power connection the power supply which allows for more headroom and the ability to connect many fans to one 4 pin header.

Only one of the hub's connectors will have a tachometer pin if applicable.

![arctic fan hub](https://i.imgur.com/4JsouQ5.png)

#### Controllers
A fan controller is a device that controls the speed of fans, as opposed to replicating an existing signal to multiple headers. This is rarely necessary as motherboards do this well enough.

![noctua fan controller](https://i.imgur.com/kayLaOB.png)


## RGB
(WIP)
