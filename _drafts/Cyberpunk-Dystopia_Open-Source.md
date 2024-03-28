---
layout: post
title: "Critical Systems Must Be Open Source - How to Not Live in a Cyberpunk Dystopia #01"
date: 2024-01-24 16:00:00 -0700
tags: politics right-to-repair cyberpunk
category: drafts # Change this before publication
#category: Cyberpunk Dystopia
hidden: true
--- 
This is post #01 <!-- Edit this AND THE TITLE before posting -->
in a series about what we can do to make real life less 
of a cyberpunk dystopia. The first post is 
[here.](https://sudo-nano.github.io/posts/Cyberpunk-Dystopia-00/) 
This post is targeted towards a general audience. No prior knowledge is required. 
If something is unclear, please refer to the footnotes or [contact me to ask for 
clarification.](https://sudo-nano.github.io/about/)

## Introduction
**Open source** is the idea of an object's design plans or software's source code
being publicly available. While there are many ideological reasons[^1] for supporting
open source hardware and software, this post will primarily cover the practical 
reasons. While open source most often refers to software, we will discuss both hardware
and software. 

"Critical systems" here means any systems whose failure are more likely than not 
to cause serious injury (physical or otherwise) and/or loss of life. This definition
encompasses systems that would cause direct harm, such as the failure of a medical 
device or autonomous vehicles that would kill a person. It also encompasses systems that 
would cause indirect harm, such as the failure of a banking system preventing people 
from accessing money needed to purchase necessities, or supply chain failures 
preventing delivery of those necessities. 

## Why Open Source? 

Closed source, or proprietary devices, have several problems:
1. They're nearly impossible to maintain if abandoned by the original developers.
2. Security research is severely hampered.
3. Accountability auditing, i.e. checking that the devices work how the manufacturer
says they do, is much harder. 

### Eliminating Abandonware 
**Abandonware** is hardware or software that is no longer being supported by the 
manufacturer. For example, Windows XP's extended support by Microsoft was ended 
on April 8, 2014. It no longer receives updates, with only a few rare exceptions 
to patch serious security vulnerabilities. Because Windows XP is no longer supported, 
there are tons of unpatched vulnerabilities that would allow someone to easily gain 
control of your computer, so it's now unsafe to connect Windows XP computers to 
the internet.

Another major consequence of abandonware is losing compatibility with current equipment. 
As new hardware and software comes out, existing things must be updated to include 
support for the new stuff. This happens on both the hardware and software level, 
but is usually worse on the software level. For example, 
older devices that only have dated interfaces like [FireWire](https://en.wikipedia.org/wiki/IEEE_1394)
or a [serial port](https://en.wikipedia.org/wiki/Serial_port) would 
be difficult to connect to a modern device that only has USB. It could be done, 
but would require an adapter that few places carry. These adapters are only available
because USB, most common serial interfaces, and FireWire are open standards: Their
specifications are publicly available for free, so anyone can design a compatible device. 

If your device requires use
of proprietary software, but the software is only compatible with an older OS like 
Windows XP, then you're likely out of luck. Unless you have an old machine running XP or someone
has reverse engineered the software and built a new version that runs on your computer, 
you have no way to use that device anymore. Reverse engineering is extremely time 
intensive and highly skilled work. In many cases, the EULA (End User License Agreement) 
or Terms of Service will outlaw reverse engineering, so even if it's viable, it's not legal. 

It's quite easy to see where this leads if these devices are controlling critical infrastructure. 
If a piece of an old system dies, replacements are no longer available, and new 
equipment isn't compatible, then you have to rip out the whole system and replace
it at great expense. This will either lead to the intentional shutdown of critical 
systems while they are painstakingly rebuilt, or a dangerous condition where they 
are inoperable but users are not informed. The damage is multiplied if the system
maintainer in question is a municipal government or similar body that provides great 
benefit to citizens but operates on extremely thin margins. 

Companies love the idea of forcing maintainers to prematurely purchase new systems, 
because it means you have to give them more money. 
Understandably, people who like their systems to work hate this. Corporations
have previously not done this often, because breaking compatibility in a way that's 
expensive for their customers generates bad PR. However, recent conglomeration
of companies due to weak antitrust enforcement means that their customers often 
have nowhere else to turn, so those companies are free to screw their customers
as hard as they want.[^2]

Requiring critical systems to be open source means that if those systems are abandoned, 
the community of people that use them can step in to maintain them, preventing otherwise
inevitable disruption of important infrastructure. 


### Assisting Security Research 
Outline: 
- Everyone benefits from security research 
- Security research functions best as a preventative measure 
- Touch on current state of security research 
- Closed source means that security researchers can only do "black box" analysis
- "white box" analysis is more productive 
- Open source exposes weak "security by obscurity"


### Accountability Auditing 
Outline: 
- 

## Footnotes

[^1]: [https://en.wikipedia.org/wiki/GNU_Manifesto](https://en.wikipedia.org/wiki/GNU_Manifesto)
[^2]: This statement applies primarily to the United States, which has fallen behind in antitrust enforcement and consumer protection laws since the Reagan administration.



