---
layout: post
title: Atom helper cpu use
modified: '2019-10-26 T18:17:25.000Z'
categories: blog
excerpt: "How to solve the probelm with Atom helper using up more than 100% of cpu and stalling Mac OSX"
tags:
  - mac osx
  - Atom helper
  - cpu
image: avg-trmm-3b43v7-precip_3B43_trmm_2001-2016_A
date: '2018-01-09 11:27'
comments: true
share: true
---

The <span class='app'>Atom</span> helper can consume more than 100% cpu on Mac OSX. My old macbook pro (early 2011) becomes unbearable slow, but I like  <span class='app'>Atom</span>, especially for producing my blog posts.

To get a manageable load on the cpu, I finally found two ways to make it work: remove all hidden <span class='file'>.git<(span)> directories and always starting <span class='terminalapp'>Atom</span> from the commandline and in safe mode:

<span class='terminal'>$ atom --safe<(span)>
