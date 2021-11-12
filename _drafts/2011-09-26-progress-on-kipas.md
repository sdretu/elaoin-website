---
layout: post
title:  "Progress on KiPas"
date:   2011-09-26 15:43:18 +0100
tags: blog kipas
---
Just an update about current development status of KiPas:

I baked a few screenshots from the Beta, taken from the real-world PlayBook (I love how you can take screenshots by simply pushing both volume keys on the PB) nothing really exciting yet, but it shows the DB Browser, an entry displayed and the open DB screen, I will add skins to make it look nicer.

<!--more-->

![KiPass Beta Welcome Screen on the PlayBook](/assets/kipas1.jpg)

![Typing Password](/assets/kipas2.jpg)

![Display an Entry](/assets/kipas3.jpg)

DB decrypting and encrypting is done, supports all password and/or keyfile method, support will be limited to KeePass 1.40 series for a start, also only AES is supported now, I will try to have TwoFish done as soon as possible, but I don’t wan’t to delay the release too much, so if TwoFish encryption is not ready for release in beginning of October, it will come in a later update.

As of now, editing is still not possible, though this is only a UI matter, as I said, encryption and saving is coded, so for the first release (wich I expect to be around beginning October) there will be support for creating and editing KeePass databases.

I have rewritten the user interface in Flex, so I am now aiming KiPas not only for the PlayBook, but also Android tablets and iPad, and eventually AIR Desktop versions, though the priority remains on the PlayBook.