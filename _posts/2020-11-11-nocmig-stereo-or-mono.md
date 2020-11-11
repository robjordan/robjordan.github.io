---
layout: post
title: "Nocmig: Are two mics better than one?"
author: Rob
summary: We've been recording nocturnal bird migration sounds for a year, using two mics near the focal point of a parabolic dish to make a stereo recording. But neither mic is precisely at the focal point of the parabola. Would we be better to make a mono recording with a more accurately positioned single mic?
categories: update
image: http://techblog.bagu.uk/assets/dish-with-two-mics.jpg
tweet: https://twitter.com/robjordan/status/1326589302726340609
---
![Parabolic dish with two microphones](http://techblog.bagu.uk/assets/dish-with-two-mics.jpg)

We've been recording nocturnal bird migration sounds for a year, using two mics near the focal point of a parabolic dish to make a stereo recording. But neither mic is precisely at the focal point of the parabola. Would we be better to make a mono recording with a more accurately positioned single mic?

While helping someone to chose equipment to start their own nocmig journey, [Tom](https://twitter.com/tomjbirding) asked me whether we have a stereo or a mono microphone. The answer is that we have [a pair of capsule mics](https://micbooster.com/clippy-microphones/99-xlr-stereo-clippy-em172-microphone.html), which we record as two channels of a stereo pair. The two mics are positioned as near as possible to the focal point of [a parabolic dish](https://parabolicmicrophone.co.uk/). But, it's clearly impossible to position both mics precisely at the focal point. With a foam wind shield, the diameter of the mic is around 2.5 cm, so &ndash; if each is positioned as close as possible to the focal point &ndash; both will be at least 1.25 cm distant from the focal point in the horizontal plane (assuming the dish to be horizontal). Moreover, the arrangement of the mic clips on the central column of the dish imposes some more constraints; they can't both be clipped at the exact same point, so there will also be a small error in the vertical plane.

Does it matter? I've always had a mild concern about this, but just blundered on, trying to position each mic as near as possible to the focus. After all, two mics must be better than one, right? I naïvely assumed that the extra signal we get from having two mics, would make up for any inaccuracy. And, we'd likely get a 'richer' recording, with some impression of passage as a bird moves across the stereo field. 

Well, Tom's question prompted an experiment, and some further reading.

[This paper](https://www.wildtronics.com/parabolicaccuracy.html) from Wildtronics addresses the effect of inaccurate placement of mics relative to the focal point of the parabola. As they explain, the focus of the parabola is the point at which reflected sounds from all over the dish have traveled an equal distance from the sound source, and so should arrive simultaneously. If they arrive in synchronised manner like this, the sound waves will be in-phase, and add together to make a louder sound. This is the whole point of the parabolic dish, it amplifies distant sounds by focusing these reflections.

![Parabolic mic](https://www.wildtronics.com/images/parabolic%20reflector.png)

(*Thanks to [Wildtronics](https://www.wildtronics.com) for the diagram.*)

But at a point slightly distant from the focus, waves will arrive out-of-phase, and so cancel one another out, reducing the volume of the sound.

I wasn't certain how significant would this cancelling effect be, given two mics positioned with an inaccuracy of about 2 cm.

The Wildtronics paper clarifies this. It's frequency-related (higher-pitched sounds require greater accuracy than lower), but in short, an 8  kHz sound, such as the ubiquitous Redwing, will be seriously impaired by an inaccuracy of just 1 cm. The 1  kHz sound of a Tawny Owl will not suffer major loss unless the mic is off by 7.5 cm.

So, to the experiment. Last night I removed one of the mics, and placed the remaining one as close as possible to the focus. I would estimate that it is within 0.5 cm, assuming the focus is correctly marked on the column (and I have great faith in Andrew at [parabolicmicrophone.co.uk](parabolicmicrophone.co.uk), who seems to have done his homework).

This morning I collected the recordings and was immediately struck by just how much louder they are. For comparison, I analysed recordings between 00:00 and 03:59 (when the metaphorical night owls of Winchester have mostly disappeared from the streets), and compared them to two recent nights with similar weather (dry, light breeze Beaufort=2). We split recordings into chunks of one minute, so this data reflects the average of 240 individual clips.

|Date|Left channel (dB)|Right channel (dB)|
|----|---------------|----------------|
|11/11/2020| - | mean: -28.4, &sigma;: 3.1|
|09/11/2020| mean: -37.5, &sigma;: 2.3 |  mean: -40.0, &sigma;: 2.5 |
|07/11/2020| mean: -31.3, &sigma;: 2.7 |  mean: -34.3, &sigma;: 2.4 |

Notice that last night's mono recordings are, on average, between 3 and 12 dB louder than the recordings from either stereo channel, on either of the two comparison nights. That is to say between 40% and 200% louder (the decibel scale is logarithmic, and 6 dB corresponds to a doubling in volume). I haven't touched the gain on the recording device in between these recordings, so any difference is purely due to mic positioning.

Notice also that the standard deviation between recordings last night is slightly larger. One might draw a conclusion that the new, mono recordings also distinguish louder and quieter sounds more effectively.

I find this very interesting and consequential. It's convinced me that two mics are not better than one. Or maybe we should buy a second dish!

Let's finish off with a honking great Redwing passage, recorded in mono, of course.

<iframe width="560" height="315" src="https://www.youtube.com/embed/GbA60fORg7Y" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>