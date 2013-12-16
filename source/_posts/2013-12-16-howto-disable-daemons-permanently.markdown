---
layout: post
title: "How to disable daemons under Ubuntu 12.04 and above"
date: 2013-12-16 22:35
comments: true
categories: 
---
Ubuntu uses the [upstart](http://upstart.ubuntu.com/) system to start several services. Every service controled via upstart has a .conf file in the directory /etc/init, so you can list the available services using
<code>
ls -l /etc/init/\*.conf
</code>


To disable a service, upstart supports a ["manual"](http://upstart.ubuntu.com/cookbook/#manual) configuration element, that can be placed either in the \<service\>.conf file or in an overriding file \<service\>.override using
<code>
sudo sh -c "echo 'manual' > /etc/init/SERVICE.override"
</code>
To reenable the service just delete the .override file.

Not every service is controled via upstart, on my system e.g. nessus is controled via init.d. Services controled via init.d are configured using an executable script in /etc/init.d and links to this script, that are located in /etc/rc?.d, according to the certain runlevels. To disable such a service, the easiest option is to remove the executable flag from the script, such as

<code>
sudo chmod -x /etc/init.d/nessusd
</code>

To revert your decision, just add the executable bit again:

<code>
sudo chmod +x /etc/init.d/nessusd
</code>
