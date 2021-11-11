---
layout: post
title:  "Tutorial: getting started with OSCream on the BlackBerry PlayBook"
date:   2011-03-30 15:43:18 +0100
tags: blog oscream tutorial
---
This tutorial will help you get started with OSCream on your PlayBook. At the end of this tutorial you will have installed a Monome application on your computer, learned how to configure OSCreamServer on your computer and OSCream on the PlayBook. You will have learned the basics of using a monome to play music.

<!--more-->

## Requirements:

* A BlackBerry PlayBook
* A computer (win or mac will do)
* Both of the above connected on the same WIFI network
* Download OSCreamServer
* Download <a title="Max/MSP runtime environment" href="http://cycling74.com/downloads/">Max runtime environment</a> - the Max runtime is available for free
* Download Stretta's <a title="Press Cafe" href="http://docs.monome.org/lib/exe/fetch.php?media=app:press_cafe2.1.zip">Press Café</a> version 2.1 for monomeserial

## Install a Monome Application (Stretta's Press Café for Max/MSP)
Download and install the Max5 runtime environment. We need it to run Press Cafe.

Unzip Press cafe to the directory of your choice, run the application by launching the file _Press Cafe.maxpat_, this will launch Press Cafe inside the Max5 Runtime.

![Press Cafe application running in Max5 Runtime. Note the prefix in the upper right hand corner.](/assets/Press_Cafe.png)

## Connect OSCreamServer
1. Run OSCream Server on your computer, if your JAVA runtime environment is properly configured, just doubleclicking the OSCreamServer.jar file will launch the app, no need to install anything.
2. You can leave all the default values, in the PlayBook TCP connection part, note the Port number. Click the Connect button.

![OSCreamServer on Windows 7](/assets/OSCreamServer.png)

## Connect the PlayBook
1. Run OSCream on your PlayBook, Swipe-Down the configuration menu from the top of the screen.
2. In the host field, enter your computer's IP address
3. In the port field, enter the port as seen in OSCreamServer Playbook TCP connection section (8090 if you kept the default settings)
4. In the prefix field type "/press_cafe" as seen in the upper right hand corner of the Press Cafe application.
5. Switch the connection ON.
6. Press any button on the PlayBook, hear the music played on your computer by Press Cafe :-)

![Press Cafe being played on the blackBerry PlayBook](/assets/PlayBookPressCafe.png)

## Going further
The <a title="monome.org" href="http://monome.org/">Monome</a> website is the best place to find lots of information about everything Monome. It has a special page referencing <a title="Monome Applications" href="http://docs.monome.org/doku.php?id=app#application_list">all monome applications</a>.

Learn more about the Open Sound Control protocol on <a title="Open Sound Control" href="http://opensoundcontrol.org/">opensoundcontrol.org</a>

For this tutorial, we relied on Max/MSP, having the Max/MSP runtime environment set up is a great plus as as many good monome application are running on Max/MSP. But there are many other software that can be used to interface with the Monome. <a title="Oure Data" href="http://puredata.info/">Pure Data</a> is an open source equivalent of Max/MSP, <a title="Chuck" href="http://chuck.cs.princeton.edu/">Chuck</a> is a music oriented programming language, or you can start programming your own Monome application in the language of your choice :-)
