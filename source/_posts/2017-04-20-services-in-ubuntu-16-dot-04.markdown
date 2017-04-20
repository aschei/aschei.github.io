---
layout: post
title: "Services in Ubuntu 16.04"
date: 2017-04-20 23:37:09 +0200
comments: true
categories: Technical 
---

Ubuntu since 14.04 switches to [systemd](https://freedesktop.org/wiki/Software/systemd/) to manage services. Time to
learn something new.

Key to systemd is the command <code>systemctl</code>

Disable a service (so that it does not start when system reboots):<br>
<code>sudo systemctl disable mongodb</code>

Enable a service (for automatic startup when system reboots):<br>
<code>sudo systemctl enable mongodb</code>

Start / Stop a service:<br>
<code>sudo systemctl start mongodb</code><br>
<code>sudo systemctl stop mongodb</code><br>

Further helpful tweaks for systemd on [this page](https://wiki.ubuntuusers.de/systemd/Service_Units/).
See also [this](/blog/2013/12/16/howto-disable-daemons-permanently/) former post about upstart and systemv runlevels.
