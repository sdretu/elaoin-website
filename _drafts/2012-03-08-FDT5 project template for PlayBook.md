FDT5 project template for PlayBook

It’s at BBDevCon that I first heard of FDT, I immediately downloaded it when I came back, and I’m now using it as my main IDE for AS3 development. While FDT5 is a great tool, it lacked default project wizards for the BlackBerry PlayBook, fortunately, this can be easily fixed thanks to FDT’s Project Templates.

In this post, we will explain how to customize FDT to create custom project templates for the BlackBerry PlayBook.

Project Templates syntax is covered in great details in the FDT documentation: http://fdt.powerflasher.com/docs/Project_Templates, so we won’t go to deep here, we will just guide through setting up a nice PlayBook project template to kick-start your PlayBook development on FDT.

What we’re trying to achieve is resumed by the two screenshots below



 

 

We’ll add a BlackBerry target to the standard Mobile/AS3 FDT project, and it will automatically generate a blank PlayBook project, with the appropriate default config files.

Project template structure

FDT’s project templates are configured through a set of config files laying in your user directory, by default on OSX the path is: (Your User Name) > Library > Application Support > FDT, while for windows 7 it is  C:Users{Username}AppDataRoamingFDT, this article covers windows, but it shall work the same on Mac.

Browse to the /FDT/projectTemplates folder, it contains a set of folder and files:


Do you recognize something? Yes, these folders correspond to the project templates type you see in the « New FDT project » window. The one we want to modify is the Mobile AS3 project, to add a BlackBerry option to the target platform list. Browse to the /FDT/projectTemplates/Mobile/AS3/project folder, this is where the definitions files are located for a Mobile/AS3 project.

Where the magic happens Description.xml

The main file for the project definition is the  /Mobile/AS3/project/description.xml, it contains all the information about the settings for that particular type of project, and what default files or directory structure should be created for that type of project. Below is the description.xml file modified to add the BlackBerry target.

<?xml version="1.0" encoding="UTF-8"?>
<tns:projectTemplate xmlns:tns="http://fdt.powerflasher.com/ProjectTemplate" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://fdt.powerflasher.com/ProjectTemplate ../../projectTemplate.xsd">
<name>AS3</name>
<version>2.3</version>
<description>This template will create the project '${projectName}' that contains only the basic libraries to develop and compile an AS3 mobile application.</description>
<projectType>AS 3 Mobile</projectType>
<variables>
<primaryGroup label="">
<variable name="appId" label="Application ID:" default="com.powerflasher.SampleApp" type="string" />
<variable name="appName" label="Application Title:" default="My Application" type="string" />
<variable name="appVersion" label="Application Version:" default="0.0.0" type="string" />
<variable name="targetPlatform" label="Target Platform:" default="Android" type="enum('Android','iOS','BlackBerry')" />
</primaryGroup>
</variables>
<projectPlatforms>
<mobilePlatform>${targetPlatform}</mobilePlatform>
</projectPlatforms>
<expressions>
<expression name="postFileName" value="replaceRegex(${projectName}, '([^w]+)', '')" />
<expression name="fileName" value="replaceRegex(${postFileName}, '(^d+)', '')" />
<expression name="postPackageStructure" value="replaceRegex(${appId}, '([.]+)', '/')" />
<expression name="packageStructure" value="replaceRegex(${appId}, '([.]+)', '/')" />
<!-- Folders -->
<expression name="sourceFolder" value="'src'" />
<expression name="outputFolder" value="'bin'" />
</expressions>
<folders>
<sourceFolder>${sourceFolder}</sourceFolder>
<outputFolder>${outputFolder}</outputFolder>
<autoLibFolder>lib</autoLibFolder>
</folders>
<contentCreation processFileExtensions="mxml,xml,launch,properties,as">
<file src="as/start.as" dest="${sourceFolder}/${packageStructure}/${fileName}.as" />
<!-- app descriptor -->
<file src="xml/start-app.xml" dest="bin/${projectName}-app.xml" process="true" if="${targetPlatform}=='Android'"/>
<file src="xml/start-ios-app.xml" dest="bin/${projectName}-app.xml" process="true" if="${targetPlatform}=='iOS'"/>
<file src="xml/start-blackberry-app.xml" dest="bin/${projectName}-app.xml" process="true" if="${targetPlatform}=='BlackBerry'"/>
<file src="xml/bar-descriptor.xml" dest="bin/bar-descriptor.xml" process="true" if="${targetPlatform}=='BlackBerry'"/>
</contentCreation>
</tns:projectTemplate>

Few things were changed from the original, first the line

<variable name= »targetPlatform » label= »Target Platform: » default= »Android » type= »enum(‘Android’,’iOS’,’BlackBerry’) » />

is where we add a BlackBerry entry to the « Target Platform » selector.

Second, we just want to add customized *-app.xml application descriptor file, and the bar-descriptor.xml (previously know as blackberry-tablet.xml)

This is done with the two lines

<file src= »xml/start-blackberry-app.xml » dest= »bin/${projectName}-app.xml » process= »true » if= »${targetPlatform}==’BlackBerry' »/>

<file src= »xml/bar-descriptor.xml » dest= »bin/bar-descriptor.xml » process= »true » if= »${targetPlatform}==’BlackBerry' »/>

You can see these two lines point to tow src files, these are the original files that we will copy to the final project folder.

We kept them in the xml subfolder of the default FDT Mobile AS3 project, as you can see, the path is relative to the position of the description.xml file.

Adding specific project files

These two files will be exactly what we want them to be in the final project, except we will use some special markup to insert the variables like project name, application ID and version.

The start-blackberry-app.xml will be almost the same as the existing start-app.xml, but you might want to strip-out the Android and iOs specific parts if you don’t plan to port your app to these platform.

A default bar-descriptor is shown below

<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<qnx>
<initialWindow>
<systemChrome>none</systemChrome>
<transparent>false</transparent>
</initialWindow>
<!-- Name of author which is used for signing.
Must match the developer name of your development certificate -->
<!-- <author>Sample Inc.</author> -->
<!-- Unique author ID assigned by signing authority. Required if using debug tokens -->
<!-- <authorId>ABC1234YjsnUk235h</authorId> -->
<!-- The category where the application appear. Either core.games or core.media-->
<!-- <category>core.games</category> -->
<!-- The icon for the application which should be 86x86 -->
<!-- <icon>
<image></image>
</icon> -->
<!-- The splashscreen that will appear when your application is launching. Should be 1024x600. -->
<!-- <splashscreen></splashscreen> -->
<!-- The permissions requested by your application. -->
<!-- <permission>access_shared</permission> -->
<!-- <permission>record_audio</permission> -->
<!-- <permission>read_geolocation</permission> -->
<!-- <permission>use_camera</permission> -->
<!-- <permission>access_internet</permission> -->
<!-- <permission>play_audio</permission> -->
<!-- <permission>post_notification</permission> -->
<!-- <permission>set_audio_volume</permission> -->
<!-- <permission>read_device_identifying_information</permission> -->
<!-- Fourth digit segment of the package version. First three segments are taken from app
description versionNumber tag. Must be an integer from 0 to 2^16-1 -->
<!-- <buildId>1</buildId> -->
<!-- Required if using ANE -->
<!-- <action system="true">run_air_native</action> -->
</qnx>

That’s it, pretty simple, let me know if you have any questions or comment.

Comments:

9 MAI 2012 À 19 H 44 MIN
Hi, integration with FDT only comes with the latest BB10 AIR SDK, and it will only work with the upcoming FDT 5.5 version, a Beta has been released a few weeks ago, and the final FDT 5.5 will be out soon.
With FDT 5.0, and previous BB AIR SDK, there was no integration of BlackBerry tools with FDT.