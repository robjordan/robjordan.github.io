---
layout: post
title:  "DIY Dummy Speaker Load"
date:   2020-08-30 00:00:00 +0100
categories: update audio 
---
I recently finished a build of a [Squeezebox](https://en.wikipedia.org/wiki/Squeezebox_(network_music_player)) with integrated class D amplifier (of which I hope to write more later).

While I still had it on the bench, before putting it into production use, I wanted to run some simple tests, inspired by the great YouTube channel of [JohnAudioTech](https://www.youtube.com/user/JohnAudioTech).

A dummy speaker load replaces a speaker with a resistor of similar impedance, so that an amplifier can be run at high volume against a consistent load.

![A pair of dummy loads.]({{ site.url }}/assets/dummy-load-finished.jpg)

Although I tinker a little bit with cheap amplifier boards, I don't expect to be doing this sort of thing often, so I didn't want to go overboard with a sophisticated design. I still hoped to a create a nice, simple and usable design though.

The type of power resistors used in dummy loads can generate a lot of heat when used at high power. I chose [8&#8486; 50 Watt resistors by Arcol](https://uk.farnell.com/arcol/hs50-8r-f/resistor-wirewound-8r-1-axial/dp/2678707). They are not the special low-inductance resistors that some audio users demand, but I was convinced by various YouTube videos that this would be overkill. I also wanted to be able to test at 4&#8486;, so I bought four resistors, two for each dummy load. By connecting the two 8&#8486; resistors in parallel, the resulting resistance would be 4&#8486;. 

Though rated 50 for Watts, [the datasheet](https://4donline.ihs.com/images/VipMasterIC/IC/OMIT/OMIT-S-A0004284475/OMIT-S-A0004284475-1.pdf?hkey=52A5661711E402568146F3353EA87419) shows that the resistors are only rated for 14W without a heatsink, and that a heatsink of 535 cm<sup>2</sup> is required to support the full rating. As a heatsink, I purchased for each resistor a 250x250mm sheet of 1.2mm Aluminium. Each dummy load is therefore a sandwich of two aluminium sheets, with a resistor bolted to each sheet on the inside of the sandwich. One resistor is permanenly in circuit across the binding post terminals for an 8&#8486; load, with the second resistor switchable into circuit for a 4&#8486; load.

![A pair of dummy loads.]({{ site.url }}/assets/dummy-load-internal.jpg)

![A pair of dummy loads.]({{ site.url }}/assets/dummy-load-internal-closeup.jpg)

![A pair of dummy loads.]({{ site.url }}/assets/dummy-load-top-view.jpg)

![A pair of dummy loads.]({{ site.url }}/assets/dummy-load-connectors.jpg)