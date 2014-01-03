---
layout: post
title:  "Extending linux lvm"
date:   2013-09-14 19:35:24
categories: linux lvm
---

I was running out of space on Fedora 17. I had a Windows installed side by side but I wasn't using it at all. I've backed up all data from there and removed that partition.
To do that I used gparted

sudo gparted

and formatted windows partition as lvm2 pv.

Then I launched system-config-lvm
and added that volume to my current existing logical volume.

sudo system-config-lvm

After doing that edited the properties of my current existing logical volume and by simply using the slider increased the size of it by needed amount of GB. I still left some unused space there for more flexibility in future.

 I recall that during the installation of Fedora the installer suggested to leave some GB to be allocated later as needed. But I found out where to do that only after removing Windows partition. Probably I'd have to do that in near future anyway but at the moment I could just use that free space.