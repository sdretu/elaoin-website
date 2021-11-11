---
layout: post
title:  "OSCream Server"
date:   2011-03-27 15:43:18 +0100
tags: blog oscream
---
OSCream Server is used to forward OSC Message between TCP protocol and UDP protocol.

[OSCreamServer 1.0 on Windows 7](/assets/OSCreamServer.png)

On the PlayBook, OSCream is developped in Adobe AIR environment, for security reasons UDP communication is disabled in AIR on mobile devices, so OSCream send its OSC Messages over TCP. But most monome applications are designed to exchange OSC messages over UDP, so a tool is needed to allow application to communicate with the PlayBook, OSCreamServer does just that.

OSCream Server is programmed in Java, so it will run on any machine where a Java Runtime Environment is available, you will need Java version 1.6. OSCreamServer is distributed as a single JAR file, to run OSCreamServer, simply double-click on the JAR file icon.

Download

latest version is 1.1, download OSCreamServer-1.1.jar now from our GitHub repository.
version 1.0, download OSCreamServer-1.0.jar now from our GitHub repository.

Source Code

OSCream Server source code is available on GitHub.