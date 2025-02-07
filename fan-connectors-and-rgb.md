---
title: Fan Connectors & RGB
layout: home
nav_order: 1
has_toc: true
permalink: /fan-connectors-and-rgb
---

# Fan and RGB wiring guide
Understanding PC fan wiring and RGB connections is essential for anyone building or maintaining a computer. Fans are critical for cooling components, while RGB lighting allows for customization of your system’s appearance. However, the variety of connectors and wiring configurations can be confusing for beginners.

This guide provides a straightforward explanation of the different types of fan and RGB connectors, their functions, and how they connect to your motherboard or controller. By the end, you’ll have a clear understanding of  your PC’s cooling and lighting systems work.

# Fans
## Essentials
Case fans in computers usually operate at 12V. At the most basic level, they require a positive and a negative connection to function. Simply connecting them to a 12V power source will make them spin at full speed.

However, this isn’t ideal for personal computers, where noise levels matter. To address this, computer motherboards control fan speed using two main methods: **voltage regulation** and **pulse-width modulation** (PWM). 

With **voltage regulation** the motherboard will output a voltage below 12V to spin the fan at a lower rate. 

Using **pulse-width modulation** requires a 3rd connection to supply the fan with a 5V square wave signal. This signal's duty cycle percentage will determine the fan's speed. This method essentially cuts motor power off many times per second (25,000 times to be precise!)

<p align=left><img src="https://i.imgur.com/G2VhseE.png" alt="square wave duty cycle example" style="max-width:60%;"></p> 

<!--image without timeframe: https://i.imgur.com/TAV8hpr.png-->

Lastly, many fans also have an additional tachometer connection. The fan sends a pulse through the tachometer lead twice per rotation. It's goal is to tell the system how fast the fan is spinning for more precise speed control. 
## Connectors

Fans come in all shapes and sizes, but so do their connectors. These few are the most common:
### 3 pin connector
The 3 pin connector has been widely used for years. It has 3 connections: negative and positive for **voltage regulation** and a tachometer readout. 

connecting a 4pin connector to a 3pin header is possible, given it isn't blocked by a neighbouring component/connector.


![3 pin connector pinout](https://i.imgur.com/TzcMQ8i.png) 
<br><sup>colours might not match*</sup>


### 4 pin connector
The 4 pin looks similar to it's predecessor put has an extra pin for PWM control, this is a more modern approach to speed regulation.

connecting a 3pin connector to a 4pin header is possible, voltage control will be needed for speed control.

![4 pin connector pinout](https://i.imgur.com/XAUrjZM.png)
<br><sup>colours might not match*</sup>



### Peripheral connectors
4pin Molex can frequently be found on cheap cases and case fans, they connect straight to your power supply and thus don't allow for any speed control. This applies to any direct connection to a power supply (E.g. SATA power).
![4 pin Molex pinout](https://i.imgur.com/sMkmC6o.png)
<br><sup>colours might not match*</sup>


### Proprietary connectors
As times have evolved many brands have come out with their own proprietary system for fans and RGB, there are too many to list them all. 

brands notorious for proprietary fan/RGB connectors include: Lian Li, Corsair and NZXT.

<p align=left><img src="https://i.imgur.com/ZKLg0CA.png" alt="proprietary connectors" style="max-width:70%;"></p> 



## Splitters, Hubs & controllers
What happens if you have more fans than fan headers? Don't worry, there's always a solution!

### daisy chain connectors
Some fans will come with an extra female connector chained to their main connector.
Daisy chain connectors will be missing the tachometer pin, this is normal as you can only have one tachometer readout/header.

**Attention:** *A single fan header can only supply a limited amount of current, connecting too many fans to a singular header can cause irreversible damage to your components. Consult your motherboard manual for a max current rating of the header. The power draw of a fan depends on the model, check the back of the fan for a power rating.*

<p align=left><img src="https://i.imgur.com/qfxLnnR.png" alt="daisy chain 4 pin PWM" style="max-width:70%;"></p> 


### Splitters
A splitter is a cable that splits one connector into multiple. This method works with no matter the speed control method, even if there isn't any. 

Only one of the splitter's connectors will have a tachometer pin if applicable.

**Attention:** *A single fan header can only supply a limited amount of current, connecting too many fans to a singular header can cause irreversible damage to your components. Consult your motherboard manual for a max current rating of the header. The power draw of a fan depends on the model, check the back of the fan for a power rating.*

<p align=left><img src="https://i.imgur.com/NlnHwV2.png" alt="examples of splitters" style="max-width:90%;"></p> 


### Hubs
There's many types of fan hubs but most commonly they use the 4 pin PWM fan header.
These hubs replicate the PWM signal across all fans connected to the hub. They also have a power connection the power supply which allows for more headroom and the ability to connect many fans to one 4 pin header.

Only one of the hub's connectors will have a tachometer pin if applicable.

<p align=left><img src="https://i.imgur.com/4JsouQ5.png" alt="arctic fan hub" style="max-width:70%;"></p> 


### Controllers
A fan controller is a device that controls the speed of fans, as opposed to replicating an existing signal to multiple headers. This is rarely necessary as motherboards do this well enough.

<p align=left><img src="https://i.imgur.com/kayLaOB.png" alt="noctua fan controller" style="max-width:30%;"></p>  



# RGB
## Essentials
Many computer components come with embedded decorative LEDs. Usually they have more than one of these pixels chained up together. More ofthen than not they are controllable via software.

Mixing **R**ed, **G**reen and **B**lue can reproduce a broad array of colours. 

The exact hue of a colour depend on the specific LED used. White is notoriously problematic. White is in theory a blend of all 3 colours at their highest intensity, however the shade of white might differ from device to device. For this reason WRGB LEDs exist, they encorporate a dedicated white LED but this is seldom used in computers.

In addition LEDs are simple cheap diodes and are prone to failure. After some time their hue will change or they might fail. Luckily this often takes a long time to appear.

## Connectors
Theres many kinds of RGB connectors, here are the most common.

### 12V 4 pin RGB
This type of LED has 3 connectors for the 3 colours it consists of. Additionally a positive 12 volt connection supplies the LED with power. No ground pin is needed as the 3 other connections serve as ground.

Each of the three colours has an intensity range from 0 to 255. They are controlled by a PWM signal from the motherboard.
This is a simple and straightforward way of controlling LEDs but offers little flexibility as all LEDs in the chain will be the same level.

An arrow on the connector indicates the 12V pin, followed by (in order) green, red and blue.

<p align=left><img src="https://i.imgur.com/dgdF3YX.png" alt="4pin RGB connector" style="max-width:30%;"></p>  


### 5V 3 pin adressable RGB (a-rgb)
This is a more modern revision of the previous connector. It uses 3 pins: positive 5V, ground and a data connection. Every LED has an integrated circuit which translates that data do a usable RGB signal. It also relays the following data to the next LED. This allows every pixel to be adressed individually, hence the name.

Here's a YouTube video explaining the process in more detail: <https://youtu.be/rHoFqKGOPRI>.

This connector uses a 5V connection, plugging it in to the aforementioned 12V header can result in irreversible damage to your components.

<p align=left><img src="https://i.imgur.com/blPcNrs.png" alt="3pin a-RGB connector" style="max-width:30%;"></p>   



### Proprietary connectors
[See fan section](#proprietary-connectors)

## Splitters, hubs & controllers
Like with fan connectors, RGB also has ways to connect multiple devices to one header.

### Daisy chain connectors
Some devices, notably fans, will have a daisy chain connector for RGB. This allows you to hook up multiple devices using one header.

<p align=left><img src="https://support.arctic.de/products/p12-pwm-pst-rgb/If-Connecting-Multiple-Fans/006_en.gif" alt="Arctic P12 daisy chain RGb guide" style="max-width:30%;"></p> 




### Splitters
A splitter is a wire that splits the signal across multiple connectors.

<p align=left><img src="https://i.imgur.com/PS3KEY4.png" alt="RGB splitter" style="max-width:40%;"></p>  



### Hubs
A hub is an externally powered device that replicates the RGB signal across multiple headers. This is a good option if your motherboard doesn't have many a-rgb headers

Some hubs combine both RGB and fan headers, often eliminating the need for two separate devices. 

**note:** *some cases include a hub with an on-board controller. Many of them use the reset button or a dedicated LED switch to change between preset rgb styles.*

<p align=left><img src="https://i.imgur.com/sAsHtV6.png" alt="RGB and fan hub in montech case" style="max-width:60%;"></p>  
<sup>RGB and fan hub in montech case cc:reddit</sup>

###  Controllers
Unlike fan controllers, RGB controllers are quite popular. Older and budget motherboards might not have an RGB header, luckily cheap controllers exist. Many have preset RGB styles that you cycle through using a button or remote. 

Some RGB controllers can be controlled via software, connecting via an internal USB header, however they usually come with a premium price.

<p align=left><img src="https://i.imgur.com/xxVtDzu.png" alt="examples of RGB controllers" style="max-width:80%;"></p> 


# Useful links
How to install a fan: <https://support.arctic.de/p12-pwm-pst-rgb>

Fan control software (FOSS): <https://getfancontrol.com/>

4pin PWM connector spec: <https://web.archive.org/web/20110726062453/http://www.formfactors.org/developer/specs/4_Wire_PWM_Spec.pdf>

Computer fan control wiki page: <https://en.wikipedia.org/wiki/Computer_fan_control>

RGB colour model wiki page: <https://en.wikipedia.org/wiki/RGB_color_model>

RGB control software (FOSS): <https://openrgb.org>

RGB control software : <https://signalrgb.com>

Microcontroller RGB control software (DIY project): <https://kno.wled.ge/>

3pin fan connector pinout: <https://allpinouts.org/pinouts/connectors/motherboards/motherboard-cpu-3-pin-fan-connector/>

4pin fan connector pinout: <https://allpinouts.org/pinouts/connectors/motherboards/motherboard-cpu-4-pin-fan/>

4pin molex pinout: <https://allpinouts.org/pinouts/connectors/power_supply/pc-peripheral-power-525/>

SATA power pinout: <https://allpinouts.org/pinouts/connectors/data_storage/serial-ata-sata-serial-advanced-technology-attachment/>

# Closing remarks
For questions feel free to join the Tech™ discord server: https://discord.gg/GtHCv2meW4
