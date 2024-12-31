---
title: How to buy a PSU
layout: home
nav_order: 1
has_toc: true
permalink: /psu
---
# What to look for when buying a PSU

There are a few key things you want your PSU to succeed at. It must:
- Not explode/catch fire/trip a breaker/otherwise threaten your safety
- Power your PC at load without crashing
- Not be loud enough to make you go deaf
- Fit in your PC (with the appropriate size and legnth for your case) with the appropriate connectors and be possible to cable manage (subjective based on cable quality, modularity helps).

You can find the necessary information from reviewers like [HWBusters](https://hwbusters.com/), [Tom’s Hardware](https://www.tomshardware.com/), [TweakTown](https://www.tweaktown.com/), [Anandtech](https://www.anandtech.com/), [Cybenetics](https://www.cybenetics.com/) and others.

## Things you care about (in order of priority):
- 12V transient response - lower voltage % change over longer time is better. Any unit that meets the ATX 3.0 or 3.1 spec is fine in this regard. Large voltage change can cause crashes with high-performance GPUs. Minor rail transients are irrelevant to most consumers, but may cause an issue for builds with many HDDs.
- Protections - Relevant ones include over-power, over-current, over-temperature, over- and under-voltage. Reviewers will note if there is an issue with any of these protections in testing. A unit with some protections missing or poorly set is not inherently bad, but can be a reliability concern. 
- Modularity and cable quality - Partially subjective, usually described with photos and opinions in reviews. High quality braided cables are generally easiest to work with, while cheap flat sleeved cables are typically seen in lower end units. Make sure ATX, EPS, 12VHPWR/12V2X6, and PCIe cables are no greater than 18AWG, preferably 16AWG. Full or Semi modular units are easier to build with but not necessarily better performing.
- Noise - lower is better. Numbers will depend on the reviewer’s methodology, but generally quiet units will measure below 25 dB and loud ones approach 40 dB at full load.
- Ripple - measured in mV, lower is better. Excessive ripple at load increases stress on VRMs and can cause coil whine or, in extreme cases, damage to hardware.
- Other platform-specific issues like APFC, multi/single 12v rail, etc

## Things you do NOT care about
- 80+ Rating - This rating does not indicate any metric of the quality of a PSU other than its efficiency. The difference in power consumption between levels of 80+ rating is extremely minor and will almost never be relevant enough to be a financial concern. Most (but not all) good power supplies will be 80+ gold or higher simply because higher quality platforms tend to be more efficient, but there are bad units at all 80+ ratings.
- Brand - Most power supplies are made by OEMs such as CWT, HEC, High Power, Andyson, and others. These OEMs are not affiliated with the brand that a given PSU is marketed under. This is to say, “Corsair power supplies are generally reliable” would be a meaningless statement since Corsair currently markets units from four separate OEMs.
- Electromagnetic interference - Some people care about this. I’m truly baffled as to why.

## Extra notes
- There is no need to over-provision wattage for a power supply. While PSUs are most efficient at around 50% load, they are designed to deliver 100% of their rated capacity to the PC. Generally speaking, CPU power limit + GPU power limit + 15 W per HDD + 100 W for the rest of the system is plenty. 
- If a given power supply does not have accurate review data but has been publicly dismantled to determine its platform (common on release of new models), you can usually cross-reference reviews of other units known to use the same platform, per the [Cultists spreadsheet](https://docs.google.com/spreadsheets/d/1eL0893Ramlwk6E3s3uSvH1_juom7SMG5SCNzP2Uov8w/edit).
- Any unit that cannot deliver its full capacity to the 12v rail per the table in its spec sheet should be avoided. 
- Multi-rail PSUs have fallen out of fashion with ATX 3.0 requiring 600 W per 12v rail at high wattages. However, if you do get a multi-rail unit, consult its documentation when plugging in cables to make sure you don’t overload a rail and trip per-rail OCP. Generally, I prefer to recommend single-rail units unless there is a particularly enticing multi-rail alternative.
- Extension cables can cause a fire hazard and should not be used when full custom cables are an option. If you do use extensions, don’t cheap out and make sure they’re high quality 16AWG cables.
- Many small form factor cases that advertise ATX PSU support become prohibitively difficult to build in with units longer than 150 mm. Many extremely small form factor cases become prohibitively difficult to build in with SFX-L power supplies. PCPartPicker does not differentiate between SFX and SFX-L for compatibility checking.
- When in doubt, pretty much all B tier and higher (NOT speculative) units on the [Cultists tier list](https://cultists.network/140/psu-tier-list/) are good enough, though this is NOT an endorsement of their methodology for segregating models into tiers.
