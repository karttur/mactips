---
layout: post
title: Recover deleted files
categories: blog
excerpt: "Time machine settings"
tags:
  - mac osx
  - Timemachine
image: avg-trmm-3b43v7-precip_3B43_trmm_2001-2016_A
modified: '2019-12-29 T18:17:25.000Z'
date: '2019-12-29 11:27'
comments: true
share: true
---

## Introduction

I lost some files because of GitHub. Deleted when changing branch from master to gh-pages. I tried to recover the lost files with four different applications. The recovery attempt failed. One app did not work, the other identified between 10 and 10,000 deleted files. I recognised the 10 files, but my, almost new, machine never had the 10,000 files. At least I have never added and deleted them. I did not manage to just recover files from the folder in which they resided prior to GitHub erasing them. the recovery attempt was thus completely useless and a waste of a days work. And now I have to remove the apps as well. Which will probably cause even more headache.

### Alternative apps

I consulted the list of [Top 7 Free File Recovery Software for Mac OS X](https://7datarecovery.com/best-recovery-apps-mac/) for finding some alternative apps. From that list I tried the following:

- Disk Drill for Mac
- TestDisk for Mac
- Lazesoft Mac Data Recovery
- iSkysoft Data Recovery
- PhotoRec Recovery for Mac

### Disk Drill for Mac

The app [Disk Drill for Mac](https://www.cleverfiles.com/disk-drill-mac.html) found thousands and thousands of files, none of which I recognized. I did not find the deleted images I was looking for.

### TestDisk for Mac

Terminal based. Could not identify disks properly. Might have to do with the new Mac OSX disk format (AFPS).

### Lazesoft Mac Data Recovery

Did not run on Mac OSX 10.14.

### iSkysoft Data Recovery

Scans the complete disk despite that I asked for a specific folder. That scan took 2 hours. Thousands (but not tens of thousands like for Disk Drill) were identified, but none that I was looking for. And I still have no idea where all the deleted files came from.

### PhotoRec

Comes in the same <span class='app'>Terminal</span> based app as TestDisk. And again the disk volumes on my Mac OSX 10.14 platform were not properly recognised. Here is a samll manual on [Using PhotoRec to Recover](https://havecamerawilltravel.com/photographer/photorec-recover-photos-memory-card/).

## Remove the apps

I manually removed the apps, seeking for leftover files under the ~/Library. As following the instructions on [How to Uninstall Disk Drill](https://nektony.com/how-to/uninstall-disk-drill).
