---
layout: post
title:  "Tutorial: getting started with OSCream on the BlackBerry PlayBook"
date:   2011-03-30 15:43:18 +0100
tags: blog oscream tutorial
---
This tutorial will help you get started with OSCream on your PlayBook. At the end of this tutorial you will have installed a Monome application on your computer, learned how to configure OSCreamServer on your computer and OSCream on the PlayBook. You will have learned the basics of using a monome to play music.

<!--more-->

<h2>Requirements:</h2>
<ul>
  <li>A BlackBerry PlayBook</li>
  <li>A computer (win or mac will do)</li>
  <li>Both of the above connected on the same WIFI network</li>
  <li>Download <a title="OSCream Server" href="http://www.smugrik.org/osc/oscream-server/">OSCreamServer</a></li>
  <li>Download <a title="Max/MSP runtime environment" href="http://cycling74.com/downloads/">Max runtime environment</a> - the Max runtime is available for free</li>
  <li>Download Stretta's <a title="Press Cafe" href="http://docs.monome.org/lib/exe/fetch.php?media=app:press_cafe2.1.zip">Press Café</a> version 2.1 for monomeserial</li>
</ul>
<h2>Install a Monome Application (Stretta's Press Café for Max/MSP)</h2>
Download and install the Max5 runtime environment. We need it to run Press Cafe.

Unzip Press cafe to the directory of your choice, run the application by launching the file _Press Cafe.maxpat, this will launch Press Cafe inside the Max5 Runtime.

[caption id="attachment_549" align="aligncenter" width="300" caption="Press Cafe application running in Max5 Runtime. Note the prefix in the upper right hand corner."]<a href="http://www.smugrik.org/wp-content/uploads/2011/03/Press_Cafe.png"><img class="size-medium wp-image-549" title="Press Cafe v2.1 in Max5 Runtime" src="http://www.smugrik.org/wp-content/uploads/2011/03/Press_Cafe-300x168.png" alt="Press Cafe" width="300" height="168" /></a>[/caption]

<h2>Connect OSCreamServer</h2>
<ol>
  <li>Run <a title="OSCream Server" href="http://www.smugrik.org/osc/oscream-server/">OSCream Server</a> on your computer, if your JAVA runtime environment is properly configured, just doubleclicking the OSCreamServer.jar file will launch the app, no need to install anything.</li>
  <li>You can leave all the default values, in the PlayBook TCP connection part, note the Port number. Click the Connect button.</li>
</ol>
[caption id="attachment_550" align="aligncenter" width="300" caption="OSCreamServer on Windows 7"]<a href="http://www.smugrik.org/wp-content/uploads/2011/03/OSCreamServer.png"><img class="size-medium wp-image-550" title="OSCreamServer" src="http://www.smugrik.org/wp-content/uploads/2011/03/OSCreamServer-300x236.png" alt="" width="300" height="236" /></a>[/caption]
<h2>Connect the PlayBook</h2>
<ol>
  <li>Run OSCream on your PlayBook, Swipe-Down the configuration menu from the top of the screen.</li>
  <li>In the host field, enter your computer's IP address</li>
  <li>In the port field, enter the port as seen in OSCreamServer Playbook TCP connection section (8090 if you kept the default settings)</li>
  <li>In the prefix field type "/press_cafe" as seen in the upper right hand corner of the Press Cafe application.</li>
  <li>Switch the connection ON.</li>
  <li>Press any button on the PlayBook, hear the music played on your computer by Press Cafe :-)</li>
</ol>
[caption id="attachment_551" align="aligncenter" width="300" caption="Press Cafe being played on the blackBerry PlayBook"]<a href="http://www.smugrik.org/wp-content/uploads/2011/03/PlayBookPressCafe.png"><img class="size-medium wp-image-551" title="PlayBook Press Cafe" src="http://www.smugrik.org/wp-content/uploads/2011/03/PlayBookPressCafe-300x176.png" alt="PlayBook Press Cafe" width="300" height="176" /></a>[/caption]
<h2>Going further</h2>
The <a title="monome.org" href="http://monome.org/">Monome</a> website is the best place to find lots of information about everything Monome. It has a special page referencing <a title="Monome Applications" href="http://docs.monome.org/doku.php?id=app#application_list">all monome applications</a>.

Learn more about the Open Sound Control protocol on <a title="Open Sound Control" href="http://opensoundcontrol.org/">opensoundcontrol.org</a>

For this tutorial, we relied on Max/MSP, having the Max/MSP runtime environment set up is a great plus as as many good monome application are running on Max/MSP. But there are many other software that can be used to interface with the Monome. <a title="Oure Data" href="http://puredata.info/">Pure Data</a> is an open source equivalent of Max/MSP, <a title="Chuck" href="http://chuck.cs.princeton.edu/">Chuck</a> is a music oriented programming language, or you can start programming your own Monome application in the language of your choice :-)
