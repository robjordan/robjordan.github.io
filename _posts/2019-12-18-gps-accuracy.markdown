---
layout: post
title:  "Investigating the Tracking Accuracy of GPS devices"
date:   2019-12-19 00:00:00 +0100
categories: update cycling gps python
image: https://github.com/robjordan/gps-accuracy/raw/master/images/error-visualisation.png
---
I'm a cyclist, and I take part in long-distance events such as the 2016 Transcontinental Race (4,000km, unsupported, from Belgium to Turkey or Greece), Paris-Brest-Paris, and long Audax events up to 600km. At the end of such a long event, I want a GPS track to document my route. Sometimes it's just for interest and posterity, but in some events, the GPS track is required to validate completion.

As a result I've developed a mild obsession with designing and building a simple GPS tracker with very long battery life, that could be used alongside more functional navigation devices. Belt and braces if you like.

The motivation for this piece of work was to discover whether there is any significant difference in the ability of GPS devices to acccurately track a planned route. The devices include popular dedicated GPS devices from Garmin and Lezyne, several Android phones, and two home-built GPS devices. I had some concerns about the accuracy of my home-built devices, and also one of my Android phones, and therefore wanted an objective way to evaluate their accuracy. To this end, I developed a Python script.

The project is [documented more fully here](https://robjordan.github.io/gps-accuracy/)  and the findings are [reported here](https://robjordan.github.io/gps-accuracy/findings). 