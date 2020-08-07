---
layout: post
title:  "Digitising 35mm slides quickly using a projector, DSLR camera and a microcontroller"
date:   2020-01-20 00:00:00 +0100
categories: update photography arduino microcontrollers esp8266
---
We have a large collection of 35mm photo slides. Some were taken by my father-in-law in the 1950s, 60s, 70s and 80s. Some were taken by me or my wife in the 80s and 90s.

I want to digitise these, and I took inspiration from various projects documented on the web, the common approach being to use a DSLR camera and a Kodak Carousel slide projector. I used an ESP8266 microcontroller to trigger the projector to advance form slide to slide, and trigger the camera to take photos.

The project is [documented more fully here](https://robjordan.github.io/projector-control/). With my rather ancient Panasonic G1 camera, and a class 10 memory card, I found I could take process one slide (with three bracketed images) in around 6 seconds. Thus a full, 80-slide carousel can be processed, unattended, in about 8 minutes.
