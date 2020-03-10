---
layout: post
title: Customize Atom
modified: '2019-11-06 T18:17:25.000Z'
categories: blog
excerpt: "Customize Atom autocomplete"
tags:
  - mac osx
  - google scholar

image: avg-trmm-3b43v7-precip_3B43_trmm_2001-2016_A
date: '2019-12-03 11:27'
comments: true
share: true
---

## Introduciton

Having used <span class='app'>Atom</span> for some time (2 years), it is in general great but it has some very silly behaviours with the default installation. First of all it consumes an enormous amount of computing power (at least on Mc OSX) and the autocomplete function is just straight stupid. Here is how to fix those things.

### Atom processor use

it is the <span class='app'>Atom</span> helper functions that eats all the RAM. You can get passed that by starting <span class='terminalapp'>Atom</span> at the terminal and in <span class='terminal'>--safe</span> mode.

<span class='terminal'>$ Atom --safe</span>

### Autocomplete

Later versions of <span class='app'>Atom</span> rely on the package _autocomplete-plus_. To edit the settings, or completely disable, _autocomplete-plus_, go via the menu:

<span class='menu'>Atom -> Preferences</span>.

In the list that opens, choose <span class='menu'>Packages</span>

A new column opens in the view, and at the top it states the number of **Installed Packages**. In the search box <span class=textbox>Filter packages by name</span>, you can write the name of the installed package to edit or disable. You can also scroll down the complete list of the installed packages.

#### Autocomplete-plus

Type _Autocomplete-plus_ in the search box <span class=textbox>Filter packages by name</span>. Click Settings to open the list of options available for changing how _Autocomplete-plus_ works.

if you want to get rid of the (stupidity) of changing words upon hitting the _Enter_ key, change _Keymap For Confirming A Suggestion_ to just _tab_ (from the default _tab and enter_)

If you think there are too many suggestions appearing overall, change the _Minimum Word Length_ from the default (3) to a higher number.

Or just disable the whole package.


#### github

If you are not using Atom with GitHub.
