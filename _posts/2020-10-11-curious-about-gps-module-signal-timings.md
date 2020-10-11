---
layout: post
title: Curious about GPS module signal timings?
author: Rob
summary: I've long been curious about the timings of GPS module signals, and whether the pulse-per-second (PPS) signal could be used to wake up a sleeping GPS. Now I have the answer.
categories: update
image: http://techblog.bagu.uk/assets/gps-neo-7n.jpg
tweet: https://twitter.com/robjordan/status/1315282226838417413
---
A short note for the record.

I've [built a few GPS devices](http://www.jordan-maynard.org/2018/03/a-gps-tracker-for-ultra-endurance-cyclists/), motivated by desire to track my bike rides. Battery life is an issue, and the general pattern of the firmware design in the controlling processor is pretty standard:

1. Wait for a message from the GPS module.
2. Decode and store the message.
3. Put the controller into a battery-saving sleep state for a period just less than the interval between GPS messages.
4. Wake up when a timer expires.
5. Go to step 1.

Part of the battery efficiency consideration is to minimise the time waiting in step 1. Since the controller is in full battery-consuming mode during that period, spending too long in that step will waste battery capacity.

GPS modules generally also output a timing signal, generally known as PPS, for pulse-per-second. A possible tiny efficiency improvement might be possible if the controller could be woken, not by expiry of a timer, but by the hardware signal provided by the PPS. 

I've looked at the datsheets for several GPS modules and never found a clear indication of the relationship between the PPS signal, and the output of GPS tracking messages on the Transmit (TX) pin. It would be convenient if the PPS signal occurred just before messages appear on TX, with just enough time to arm the UART to receive the data.

Now I have an oscillosope I can finally answer the question, at least for one GPS module. I conducted an experiment with a Chinese module, ostensibly based on a U-blox NEO-7N GPS receiver. Most likely the chip is a fake, but perhaps the findings hold true for genuine U-blox receivers.

![NEO-7N GPS module]({{ site.url }}/assets/gps-neo-7n.jpg)

As the images below show, the signals are organised as follows. The PPS signal, normally low, goes high for about 100ms every second. As it happens, in these traces, GPS location messages are transmitted every two seconds. This is configurable. The GPS messages commence about 50ms after the rising edge of the PPS signal. So it does seem there is some possibility to use the PPS as a trigger to wake the controller. Whether this is practical will depend on a number of factors including: 
* the time a particular controller takes to wake from deep sleep and ready its UART to receive, and
* whether the specific application wants to receive GPS location information every second.

A roughly three second trace, showing PPS (pink, normally low) and TX (yellow, normally high).
![A 3 second trace, showing PPS (pink) and TX (yellow)]({{ site.url }}/assets/SDS00001.png)

Zooming in, 54ms between PPS rising edge and TX commencing.
![54ms between PPS rising edge and TX commencing]({{ site.url }}/assets/SDS00002.png)

100ms duration of PPS.
![100ms duration of PPS]({{ site.url }}/assets/SDS00003.png)