---
layout: post
title:  "Experiences buying and burning replacement EPROMs for 2716-type devices"
date:   2020-08-28 00:00:00 +0100
categories: update retrocomputing 
---
I'm restoring my first home computer, a 1979 [Exidy Sorcerer](https://en.wikipedia.org/wiki/Exidy_Sorcerer). I discovered a fault with one of the 2KB programmable read-only memory (PROM) chips; it had lost its memory and become blank. Terry Stewart had an identical problem, so I won't describe the [fault diagnosis process that he has documented so thoroughly](https://www.classic-computers.org.nz/blog/2011-06-25-sorcerer-rom-pac-fix-part-1.htm).

The result was that I needed to source EPROMs, more-or-less compatible with the 2716 pin layout, as well as a UV EPROM eraser and an EPROM programmmer. I researched numerous articles, and watched many videos, and while I learned a lot, I was also left with the feeling this is a minefield. Because 2716-type devices have not been manufactured for many years, there is great suspicion in the marketplace. Which chips are genuine and which are fake? Which chips are compatible with which programmers?

I won't add to the ethical and economic debate about the veracity of the available chips, but simply relate my experiences which were less painful than I feared.

### Programmer
I bought a [TL866 II Plus Universal Programmer](http://xgecu.com/TL866_main.html) from a UK-based ebay seller named [yourcartmax](https://www.ebay.co.uk/usr/yourcartmax) for £41. It was the cheapest UK-based offering. There are claims that these devices have been conterfeited, but also that the presence of a label on the bottom of the machine is suggestive of a genuine item. Here's the label on mine. I have no reason to doubt its authenticity. 

The programmer comes with software for Windows on a CD, but more recent updates are available via the [xgecu website](http://xgecu.com/). At the time of writing the latest is 10.31. You are instructed to install the software before plugging in the programmer to a USB port, so that drivers are available. Once again the fear, uncertainty and doubt is rife regarding this software. A thread indicates that six different anti-virus products detect malware. I checked it with Avast, and nothing untoward was detected.

I used a rear USB port on the elderly Dell desktop machine on which I run Windows, on hearsay grounds that the rear ports deliver more current to USB. Programming EPROMs does demand higher voltages than USB's 5V, so the programmer may be impacted by current-limited USB ports. Some people recommend a powered USB hub but I don't have one. More on this high-voltage programming later.

### Eraser
EPROMs can be erased and reprogrammed. Erasure requires exposure to light in the UVC range, ideally 254nm. There are cheap Chinese-origin plastic boxes containing a mercury vapour tube, and a little electronics, which promise to do the job. There is also lots of chatter on the boards about erasing with sunlight (you can but it takes weeks instead of minutes), toothbrush santisers, UV LEDs at close range (the lowest wavelength available from LEDs at this time seems to be 365nm, so less effective), and the usual claim that the Chinese devices are crap and you really need a used, turn-of-the-century device from eBay. With my head spinning from all the options, I ended up buying a [cheap Chinese device from Banggood](https://uk.banggood.com/NEW-High-Speed-Ultraviolet-Eraser-UV-EPROM-Eraser-Ultraviolet-Light-Erasable-Timer-p-1532425.html) for $22. Banggood seem to get things to me a bit quicker than Aliexpress, and my biggest worry was receiving a box full of broken glass and mercury droplets [like this poor fellow](https://www.youtube.com/watch?v=Zn3kWy_5kWU). Luckily all arrived intact nine days after ordering.

### Chips
Here's where things get really interesting(!) The original memory device in the Sorcerer BASIC cartridge was a masked ROM. It means the memory was one-time programmed by the chip manufacturer. EPROMs, as we've discussed, are user-erasable. As far as I can tell, [the original 2716 was an Intel device](http://www.sycelectronica.com.ar/semiconductores/2716.pdf) which is rarely found these days. Subsequently other manufacturers copied the idea and produced a variety of devices with similar-sounding names. It's named '27' because (I don't know) and '16' because it has 16k bits of storage capacity, ie 2K bytes. In the user-programmable device, pin 21 is used to supply a high voltage when programming the memory, and +5V in normal operation. Clearly a programming voltage wasn't necessary in the masked ROM, so pin 21 is wired to Ground. This means, assuming we are successful programming a replacement EPROM, we'll have to do some jiggery-pokery to get the chip working in the Sorcerer.

As I mentioned, many manufacturers followed Intel in offering 2716-style devices and these other manufacturer device types can easily be found on ebay and AliExpress. Fakes? Probably. Does it matter at this point when no western manufacturer offers new chips of this type? For my money, no. Two devices that seem commonly offered are:
- ST Microelectronics M2716-1F1
- Fairchild NMC27C16B

Both parts have the same pinout as the original Intel 2716. The letter C in between 27 and 16 indicates that the Fairchild NMC27C16 is a CMOS device. The chief benefit of CMOS technology is lower power consumption than NMOS. The active power consumption of the Fairchild NMC27C16 chip is advertised as 55mW vs 525mW for the STM M2716 part. Not that this matters much in the context of the Sorcerer which is already cooking with tens of Watts burning off in the power supply.

But more significant in the present exercise is the voltage required on pin 21 to program the memory (V<sub>pp</sub>). M2716 requires NMC27C16 reuir
