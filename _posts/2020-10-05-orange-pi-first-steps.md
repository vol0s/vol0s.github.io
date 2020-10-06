---
title: OrangePi Zero Plus 2 H5 first steps
date: 2020-10-04 19:56:00 +0000
categories: [Tutorial, OrangePi]
tags: [armbian, orangepi]  
---

[opizero-firstlogin]: /assets/img/sample/opizero-firstlogin.jpg "First login screen inside Armbian OrangePi Zero 2 H5"
[armbian-config]: /assets/img/sample/armbian-config.jpg "Armbian configuration options"


# What is OrangePi
---

[Orange Pi](http://www.orangepi.org/) is an open source single board computer, based on Raspberry Pi 1 but lower priced and manufactured by Shenzhen Xunlong Software CO.

It can work with Android versions 4, 6 or 7.0, depending on the model, Ubuntu, Debian, Fedora, Raspbian, ArchLinux, openSUSE, OpenWrt and other operating systems, although the most efficient is Armbian. It uses the AllWinner A20 SoC processor, and has a memory that goes from 256 MB of the Orange Pi Zero to the 2GB DDR3 SDRAM of the main boards. It has a standard TF card slot.

# Flashing Armbian to Orange Pi Zero Plus 2 H5
---

In this case we will be flashing `Armbian` to an Orange Pi Zero Plus 2 H5. It comes with 512MB of DDR3 SDRAM and H5 Quad-Core SoC up to 1.2GHz.

First of all, we need to visit the [Armbian](https://www.armbian.com/download/?tx_maker=xunlong) `Orange Pi` downloads page and download the latest version of the software. Armbian Focal with kernel 5.8.y for us.

Once the file is downloaded now we need to flash it to our SD Card. We will be using the official `rpi-imager` package provided by RaspberryPi people. With Armbian being based on debian, we can install it this way:

```bash
sudo apt install rpi-imager
```

The next step will be using the software to flash the image. rpi-imager will handle the extraction for us, so we just need to pick our custom image and the target SD card.

# Configuring Armbian
---

Once we flashed the image, plug in the SD card, HDMI cable and the keyboard to the OrangePi, followed by the power cable. If we did the process the right way, we obtain the following screen:

![opizero-firstlogin][opizero-firstlogin]


## Connecting to the internet
---

Due to the lack of an ethernet port, the first thing to do is connecting to the internet via the following command, which will prompt us a new WiFi connection:

```bash
sudo nmtui-connect
```

## Running armbian-config 
---

The final first steps are configuring the OrangePi in the manner of our personal needs. We can do that running this command:

```bash
sudo armbian-config
```

![armbian-config][armbian-config]
