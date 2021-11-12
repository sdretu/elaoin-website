Dynamic Range manipulation in music production

August 18th, 2013 § Leave a Comment

I am following the Coursera class “Introduction to music production”. In this post, I’ll try to explain the concepts behind dynamic range manipulations in a musical post-production context, as part of the fourth week assessment.

## What is the dynamic range

The dynamic range of a musical piece or a recording, is the difference between its loudest parts and quietest parts, controlling the dynamics helps to control the amount of energy in each part of a recording, allowing to guide the auditor through the piece, giving the focus on the relevant parts.

## Dynamic range manipulations

In music post-production, modifying the dynamics is equivalent to changing the volume of a part of a recording. There are basically two ways the dynamic range can be manipulated, it can be either compressed, or expanded.

* Compression means decreasing the dynamic range, by either making the louder parts quieter, or raising the quieter parts, or both.
* Expansion is the opposite, increasing the dynamic range, by making the louder parts even louder, or making the quieter parts even quieter, or both.

The first way to control the dynamics of a piece would be to manually adjust the volume of the recording by moving the volume slider, and recording the movements in an automation track. This could be a way to control the dynamic range over a long span of time, like making the chorus louder in comparison to the verse of a song, or adjusting the levels of different parts so they are consistent throughout the piece.

Then the volume could be adjusted on a smaller scale, for example, adjusting the levels of each words or syllables relating to each other, to help make the vocals more focused and intelligible.

When we want to control the volume at an even finer level, correcting the attack level of each note of an instrumental recording, controlling it manually, either by recording the slider movements, or drawing automation curves in a DAW, becomes tedious. So the process can be automated, by applying a simple rule like “if the volumes gets louder than this level, attenuate it, if it gets quieter than that level, raise it”, this is the purpose of dynamics processors.

* Compressors will compress the sound: if the signal goes above the threshold, make it quieter.
* Expanders make the signal quieter if it goes below a threshold.
* Limiters and gates are respectively the same as the above, but they are much more drastic in the way they modify the output.

## Dynamics processors

A dynamics processor (compressor, expander, limiter, gate) is made of two sections

* the sidechain, whose purpose is to analyze the signal, to detect variations in volume, the envelope, or anticipate these changes.
* the second part adjusts the volume according to a set of rules, and  the envelope information provided by the sidechain section.

The basic controls of a dynamics processor are the threshold, which indicates at which level it will start to modify the level, and the second parameter is the ratio, which will tell by how much the volume is to be modified when it passes the threshold level.

The attack and release parameters tell how fast the volume is changed, attack is when the signal passes above the threshold, and release is when it passes below.

The knee helps to soften the change of the volume fader as the volume reaches the threshold point.

Finally, the lookahead parameters tells the processor to react ahead of time, it sees the envelope a bit in the future, and the processor will start to react before the changes happen, so when it sees the envelope will cross the threshold level, it starts to change the volume proactively, before we reach the threshold point.