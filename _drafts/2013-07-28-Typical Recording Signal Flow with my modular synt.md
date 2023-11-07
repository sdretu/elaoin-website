---
layout: post
title:  "Typical Recording Signal Flow with my modular synth"
date:   2013-07-28 16:43:18 +0100
tags: blog ableton coursera
---

I am following the Coursera class [Introduction to music production](https://www.coursera.org/learn/produccion-musical). In this post, I’ll teach what is the typical signal flow when recording my modular synth with my own gear in my little home studio, as part of the first week assessment.

The gear I’m using here is described below:

* My Eurorack modular synthesizer
* A special output module to attenuate the audio signal of the modular to line level
* a standard TS quarter inch jack cable
* an Edirol UA-25 USB audio interface (and a USB cable)
* a Mac Mini
* A pair of Yamaha HS50M monitors (and a pair of balanced TRS jacks)

Unlike an acoustical instrument, such as a guitar, where sound starts as variable pressure in the air that needs to be converted to voltage by a transducer (a microphone), the modular synthesizer is an electronic instrument, so the sound is created directly by the synth in the form of varying voltages, and the output of the synthesizer is sent directly to the input of the UA-25 through a quarter inch TS jack.

![]()
![On the bottom right of the case is the output module, it gets input from the modular eighth inch yellow cable, and outputs it on quarter inch green jack. The red pot allow to set the output level.]()

Because the signal of a modular synth is of very high amplitude compared to the signal of a standard line level or even microphone, the signal must be attenuated before it goes to the UA-25, also the Eurorack modular format uses eighth inches jacks, whereas my audio interface as quarter inches jack inputs, so I use a special module, which takes an input at Modular level in eighth inch format, attenuates the signal, and outputs it at line level in quarter inch format.

From there, the signal goes to the audio interface, here the signal is split in two paths: the Edirol UA-25 has a so called “direct monitor” option, which transits the signal on the input directly to its outputs, without going through the computer, this is useful, because it allows to listen to the modular synthesizer directly, without the latency induced by the audio treatment in the computer.

The second signal path goes to the computer through the interface’s analog to digital converter and the usb cable. The synthesizer is then recorded in the DAW software, Ableton Live 9. in Live, I mute the track being recorded, so that it doesn’t interfere with the direct-monitor output from the interface, the other instruments tracks (like drums, bass or guitar) are played back, and sent through the USB cable to the interface’s digital to analog converters, mixed with the direct monitor signal in the interface, and the resulting mix (playback from Live + direct monitor of the modular synth) is sent to the outputs, and finally to the HS50M speakers through a balanced TRS jack, and because there is no microphone in the signal flow, I don’t have to worry about feedback from the monitors.

![Edirol UA-25]()
On the Edirol UA-25, the signal from the modular synth is coming to the input one through the green cable. on the right, notice the direct monitor section, with two switches and a volume pot, the red led next to the volume indicates the direct monitor option is activated, the mono switch sends both inputs to both outputs, so the input 1 is heard on both speakers, the output are on the back of the audio interface.

As a final reflection about this process, I would like to come back on the direct monitoring option of the UA-25 interface, because it also applies to recording electric guitar, bass or other electronic instruments. The direct monitor has its pros and cons: the pro is that it allows to hear what you are playing with no latency, so if you record an electric guitar or bass, you can plug the electric guitar directly into the audio interface, and hear what you’re playing directly from your monitors while it is being recorded in the DAW. Hence if your audio interface has such an option, you don’t need a direct box to connect your guitar to the interface and to its amp for monitoring, and if you have no proper room to record the output of the amp with a microphone, or if your guitar amplifier has no line output, the direct monitor of the audio interface is really convenient. The con is that what you hear is not what is actually recorded, any effect or processing applied in the DAW isn’t monitored when you record, but this also applies to the direct-box or amplifier line-out options.