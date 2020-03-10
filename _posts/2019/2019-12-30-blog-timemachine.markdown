---
layout: post
title: Time Machine
categories: blog
excerpt: "Time machine settings"
tags:
  - mac osx
  - Timemachine
image: avg-trmm-3b43v7-precip_3B43_trmm_2001-2016_A
modified: '2019-12-30 T18:17:25.000Z'
date: '2019-12-30 11:27'
comments: true
share: true
---

## Introduction

This short post summarizes my experience in using the SD slot on a macbook air 2017 for timemachine backup.

### Erase and partition

I got a [Transcend JetDrive Lite 130](https://www.transcend-info.com/Products/No-637) with 256 GB from [ProShop](https://www.proshop.se/Flashram-USB-Flash-Drives/Transcend-JetDrive-Lite-130-flash-minneskort-256-GB/2493950?utm_source=prisjakt&utm_medium=cpc&utm_campaign=pricesite). It was already formatted, but I wanted to create 2 partitions.

![sidebar](../../images/sidebar-select.png)
{: .pull-right}
Open the <span class='app'>Disk Utility</span>. You should see your disk in left sidebar (column). Later version of Mac OSX by default only shows the _volumes_ in <span class='app'>Disk Utility</span>, you need to expand that in order to access the physical devices as well. Click on the sidebar icon and select the alternative _show all devices_.

Erase the Jet Drive _volume_ and then you can create the partitions. I choose to partition using (Globally Unique IDentifier) GUID, the Mac OSX format for intel based machines. For details see [this](https://www.lifewire.com/apple-partition-types-2260881) page.


<figure>
<img src="../../images/partition-jetdrive.png">
<figcaption> Partition the Jet Drive Lite (SD card). I created 2 partitions, 1 for Time Machine (_mactime_) with a size equal to the internal SSD drive, and 1 additional backup partition (_jet_). </figcaption>
</figure>

### Time Machine

_Time Mashine_ is a utility that you can access from the _System Preferences..._ under the apple in the Mac OSX main menu. In the System Preferences window, Time Machine is available in the bottom row, almost as the last icon.

<figure>
<img src="../../images/system-references-window.png">
<figcaption> System Preferences window, Time Machine is available in the bottom row, almost as the last icon. </figcaption>
</figure>

#### Options

In the Time Machine utility, click the <span class='button'>Options...</span> button. Then add the folders that you want to exclude from the Time Machine backup. I excluded all applications and libraries as well as all users except my own. You must also exclude the partition on the Jet drive that you are not going to use for the Time Machine.

<figure>
<img src="../../images/time-machine-options.png">
<figcaption> System Preferences window, Time Machine is available in the bottom row, almost as the last icon. </figcaption>
</figure>

### Select Disk

Select the volume (rather than disk) to use for backup. Click the button <span class='app'>Select Disk...</span> and navigate to the Jet Drive partition (_mactime_ in my example) to use for your time machine backups.

You should be ready to go. The first backup should start after a couple of minutes.
