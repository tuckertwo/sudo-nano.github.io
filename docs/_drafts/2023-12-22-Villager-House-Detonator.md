---
layout: post
title: "Precision Villager House Detonator"
date: 2023-12-22 10:00:00 -0700
tags: video-games minecraft
---

A few years ago, I worked with some friends on a small Minecraft SMP server to take out someone who liked to combat log. While I am not proud of the circumstances, I *am* proud of this small piece of precision engineering. The combat logger in question lived in a small villager house, so I designed this precision explosive to destroy the house with minimal collateral damage. It was made to be hidden under the house, so there are no above-ground components, and it was made to be efficient, using 5 pieces of TNT as efficiently as I could manage. 

![Redstone design for villager house detonator]({{site.url}}/assets/villager_house_exploder/design.png)
*Figure 1: Precision Villager House Detonator*


![Redstone design for villager house detonator (cutaway view)]({{site.url}}/assets/villager_house_exploder/design_cutaway.png)
*Figure 2: Precision Villager House Detonator, cutaway view. Closest TNT piece and glass to viewer removed to show the restone torch that triggers the primary charge.*

The design is relatively simple, but was refined through many trials. The four pieces of TNT on the bottom make up the primary charge, which blows up the bottom of the house. The single piece of TNT on the top is the secondary charge, which is launched up by the primary charge, and destroys the top of the house. The secondary charge is lit 4 ticks after the primary charge. 

As demonstrated below, this design provides a minor improvement over a standard untimed TNT charge. 

![House detonated with a standard untimed charge]({{site.url}}/assets/villager_house_exploder/exploded_house_regular.png)
*Figure 3: A small villager house detonated using an untimed charge of 6 pieces of TNT. The roof is relatively intact.*

![House detonated with a precision timed charge]({{site.url}}/assets/villager_house_exploder/exploded_house_precision.png)
*Figure 4: A small villager house detonated using the timed precision charge detailed in this article with only 5 pieces of TNT. The roof is less intact than the previous image.*

Further research is necessary to create a more modular or scalable version of this design, to create one that more thoroughly destroys the roof, and to create one capable of destroying larger sizes of villager house. 

### Assets
The Litematica schematic for this design is available [here]({{site.url}}/assets/villager_house_exploder/precision_villager_house_exploder.litematic). 