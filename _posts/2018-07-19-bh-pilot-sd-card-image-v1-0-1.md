---
ID: 757
post_title: BH Pilot SD Card image v1.0.1
author: bithollow
post_excerpt: ""
layout: post
permalink: >
  https://bithollow.com/bh-pilot-sd-card-image-v1-0-1/
published: true
post_date: 2018-07-19 10:24:13
---
**Raspberry Pi 3 SD card image**

- kernel 4.6.5
- preempt-4.6.5-rt9
- debian 8.6 jessie armv7a hf
- raspap-webgui 1.2
- ardupilot copter 3.6.0-rc5
- ds1339 rtc enabled
- bcm43430 bluetooth enabled
- bcm43430 sdio wifi enabled
- dhcp server client ip pool changed from only `10.0.0.2` to ranged `10.0.0.2~10.0.0.253`, lease time 12 hours.
- ardupilot MAVLink message now broadcast to all the client ips.
- onboard GPS communicates via SPI bus, UART is used for terminal.

---

The sd card image split into several parts because the host limited the largest file size.

The following instrustions assumes:

- To download and join the parts under Linux (about 167MB)
- Your Raspberry Pi sd card is the device '**/dev/mmcblk0**' (change the device name according to your system)

1. Download `rpi.img.xz.part00`~`rpi.img.xz.part02` to a directory
2. In the above directory, join the parts together
  ```shell
  $ cat rpi.img.xz.* > rpi.img.xz
  ```
3. Write sd card
  ```shell
  $ sudo sh -c 'xzcat rpi.img.xz > /dev/mmcblk0'
  $ sync
  ```
4. Plug the sd card to Raspberry Pi, power on. It is for Raspberry Pi 3 only (all models)

---

- This image enabled hotspot AP by default, on your ground control station, search ssid `bithollow-bh`, default password is `bithollow`. Its dhcp server will dynamically assign client ip in the pool: `10.0.0.2~10.0.0.253`, lease time 12 hours.

   MAVLink message from ardupilot will be broadcasted to each of the leased client ip, thus you could have multiple GCS as clients to monitor ardupilot status.

- To config the hotspot AP, access `10.0.0.1` in your web broswer, user: `bit`, password: `hollow`

- If you found your GPS somehow not responsed, cut off GPS battery power by the DIP switch on BH board while Raspberry Pi is not powered on. (more information about the DIP switch is in user documents)

---

[Go to download page](https://bithollow.github.io/downloads/rpi-sd-image/2018/07/19/sd.image_v1.0.1)