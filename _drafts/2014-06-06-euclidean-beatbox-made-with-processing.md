---
layout: post
title:  "Euclidean beatbox made with Processing"
date:   2014-06-06 15:43:18 +0100
tags: blog processing sequencer
---
This is an <a title="online Euclidean beatbox" href="http://www.smugrik.org/processing/Euclidean" target="_blank">online Euclidean beatbox application</a> I did a while back when learning the basics of processing language.

The idea was to experiment with Euclidean algorithm for rhythmic patterns generation.

So this app provides three basic beatbox sounds, a kick, a snare and hi-hat, each triggered by its own Euclidean sequence. The tempo is fixed, you can adjust volume of each sound, set the length of the pattern, and the number of hits in each pattern.

<!--more-->

An euclidean sequencer, unlike a standard step sequencer, doesn't allow you to choose precisely which step in the measure will be played, rather, the rhythmic pattern is auto generated, according to an algorithm based on Euclid's work. The algorithm takes two parameters: the length of the pattern, and the numbers of hit in that pattern, one hit means one note per mesure, by raising the hit number, you will get more notes. So it is easy to change the pattern by simply adding more note ( to create a break) or less. The Euclidean algorithm generates patterns that are meaningful in musical terms, by trying to distribute the hits evenly in the pattern.

For exemple, for a length of 8 (- is silent and O is a note):

hits = 1 will give the following pattern : O - - - - - - -

hits = 2 : O - - - O - - -

hits = 5 : O - O O - O O -

hits = 8 : O O O O O O O O

All three sounds are synchronized to the same tempo, so by changing each sound pattern lenght and hits, it is possible to create intricate infinitely varying rhythmic patterns.

The best way to understand it is to simply try it!

Hear it in action here:<a title="http://www.smugrik.org/processing/Euclidean" href="http://www.smugrik.org/processing/Euclidean" target="_blank"> http://www.smugrik.org/processing/Euclidean</a>

## References
Uses the Maxim library <a title="https://github.com/micknoise/Maxim" href="https://github.com/micknoise/Maxim" target="_blank">https://github.com/micknoise/Maxim</a>

These articles about Euclidean rhythm generation and Bjorklund's algorithm:

Euclidean rhythms on Wouter Hisschemoller's blog <a style="color: #0367b0;" href="http://www.hisschemoller.com/2011/euclidean-rhythms/">http://www.hisschemoller.com/2011/euclidean-rhythms/</a>

The Euclidean Algorithm Generates Traditional Musical Rhythms by Godfried Toussaint <a style="color: #0367b0;" href="http://cgm.cs.mcgill.ca/~godfried/publications/banff.pdf">http://cgm.cs.mcgill.ca/~godfried/publications/banff.pdf</a>

Generating Musical Rhythms on Kristopher Reese's blog <a style="color: #0367b0;" href="http://kreese.net/blog/2010/03/27/generating-musical-rhythms/">http://kreese.net/blog/2010/03/27/generating-musical-rhythms/</a>
