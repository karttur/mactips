---
layout: post
title: Install Dia using Brew and XQuartz
categories: blog
excerpt: "Install Dia using Brew and XQuartz on Mac OSX 14 (Mojave)"
tags:
  - mac osx
  - Dia
  - XQuartz
  - Mojave
image: avg-trmm-3b43v7-precip_3B43_trmm_2001-2016_A
modified: '2019-12-30 T18:17:25.000Z'
date: '2019-12-30 11:27'
comments: true
share: true
---

## Introduction

[<span class='app'>Dia</span>](http://dia-installer.de/index.html.en) is a great app for creating flow charts and other diagrams. It is just at the level of complexity that I favour. At time of writing this (January 2020) the <span class='app'>Dia</span> version requires [XQuartz](https://www.xquartz.org). But installing <span class='app'>XQuartz</span> on mac OSX 10.14 (Mojave) caused me some problems. The official [XQuartz](https://www.xquartz.org) recommendation is to use <span class='terminalapp'>MacPorts</span> for installing <span class='app'>XQuartz</span>. But I use <span class='terminalapp'>Homebrew</span> instead of <span class='terminalapp'>MacPorts</span>.

This post just links to the page [Install Dia on Mac OSX at macappstore.com](http://macappstore.org/dia/) that contains the <span class='terminalpp'>Homebrew</span> code for installing <span class='app'>XQuartz</span> and <span class='app'>Dia</span> on Mac OSX 10.14 (Mojave).

## Install Homebrew

<span class='app'>Terminal</span> command for installing <span class='terminalapp'>Homebrew</span>:

<span class='terminal'>$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" < /dev/null 2> /dev/null ; brew install caskroom/cask/brew-cask 2> /dev/null</span>

When the installer finishes, install <span class='app'>XQuartz</span> using <span class='terminalapp'>brew</span>:

<span class='terminal'>$ brew cask install xquartz</span>

And then install <span class='app'>Dia</span>:

<span class='terminal'>$ brew cask install dia</span>

The installation installs <span class='app'>Dia</span> as an ordinary app in the <span class='file'>Applications<(span)> folder.

## Restart Homebrew

I could use <span class='app'>Dia</span> after having started it the first time. But trying to restart after closing it did not work. To solve that I followed the hint on the [GitHub page: How to install Dia on OSX (and have it run)](https://gist.github.com/jclosure/72cefed87528917daac9f65a2029a5dc). I opened the file <span class='file'>/Applications/Dia.app/Contents/Resources/bin/dia</span> using the terminal editor <span class='terminalapp'>pico</span>:

<span class='terminal'>$ pico /Applications/Dia.app/Contents/Resources/bin/dia</span>

and then I added the following command at line 40 (just  before the oascript call):

```
#########################################################
# Ref: http://navkirats.blogspot.de/2014/10/dia-diagram-mac-osx-yosemite-fix-i-use.html
versionOSX=$(sw_vers -productVersion | awk -F '.' '{print $(NF-1)}')
[[ ${versionOSX} -ge 10 ]] && export DISPLAY=:0
#########################################################
```

After saving the edits and then restart my Mac OSX Mojave (10.14) machine, I got <span class='app'>Dia</span> to start any time.
