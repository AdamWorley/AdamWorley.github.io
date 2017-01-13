---
layout: post
category : Projects
tagline: "| Installing Arch on Mac and PC "
tags : [OSx, Mac, Arch, C++, Uni, Linux, PC, Windows]
---

{% include JB/setup %}

So deciding to take the plunge and install arch onto my mac has been... time consuming. I'm now at a stage I'm fairly happy with (Wi-Fi and eduroam still don't get along).

### Step 1 - Setting up the Mac

For the most part following [this tutorial](http://zanshin.net/2015/02/05/arch-linux-on-a-macbook-pro-part-1-creating-a-usb-installer/) worked for me. Only real deviation was the packages to be installed once the base install had been laid down. Another issue is the Wi-Fi; due to the chip being a broadcom chip it didn't work out of the box and so needed a bit of work which leads onto...

### Step 2 - Aur you sure? ###

Setting up yaourt, just follow the tutorial [here](https://www.digitalocean.com/community/tutorials/how-to-use-yaourt-to-easily-download-arch-linux-community-packages) for all of the instructions. To use yaourt is not really any different from pacman, just use yaourt -S and the package to be installed.

The first aur package to grab is the [b43-firmware](https://aur.archlinux.org/packages/b43-firmware/) not the b43-fwcutter which is for extracting the drivers from the original driver file.

### Step 3 - Touchpad ###

The touchpad works perfectly out of the box in gnome, in KDE however the righ-click was not working. Follow the instructions [here](https://wiki.archlinux.org/index.php/Mac#Touchpad) on how to change the mtrack file and enable right-click.

### Step 4 - Private Internet Access ###

There are several ways to set-up PIA the one I opted for is to install the aur as described [here](https://wiki.archlinux.org/index.php/Private_Internet_Access_VPN#Installation) and then start it on boot using [this guide](https://wiki.archlinux.org/index.php/OpenVPN#systemd_service_configuration). This is not the best method as it will always connect to the same server and there is no simple way to disconnect or connect to an alternative, but it does start the fastest which is nice.


### Things that I have missed ###

The arch wiki has a lot of useful information so anything that has been missed can be found relatively easily. The macbook specific page is [here](https://wiki.archlinux.org/index.php/Mac).


### Things that just don't work ###

Either due to hardware limitations or closed source drivers the following don't work 100%:

- Bluetooth: Following the instructions outlined, bluetooth devices can connect however audio is glitchy and will disconnect after only a couple of minutes. File transfers have been untested.

- Suspend on laptop close: As the nvidia driver is required for smooth video and to use android studio the suspend on laptop close doesn't work; this is due to the driver not reporting the number of monitors connected, as the laptop may be docked and someone might want to close the laptop and work on an external monitor the default behaviour is to leave the laptop on and changing the config file doesn't appear to have any affect.
