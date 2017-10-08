---
ID: 700
post_title: BH v0.2 fixes schematic bugs
author: bithollow
post_excerpt: ""
layout: post
permalink: >
  https://bithollow.com/bh-v0-2-fixes-schematic-bugs/
published: true
post_date: 2015-10-20 00:31:06
---
Here comes the **BH Pilot** v0.2, fixed several bugs related to the schematic. Furthermore, we introduced the following enhencements:

- Replaced MPU6050 and HMC5883L to MPU9250. MPU9250 is the successor of MPU6050, it features Accelerometer, Gyroscope and Magnetometer all in one together. So we could remove HMC5883L for cost and software maintenance.

- Added a DIP switch. **BH** isn't for Raspberry Pi only, on other development board, such as Beagle series, Banana Pi series or Arduino series, DIP switch could effectively maintain hardware configurations.

- Enable selecting MPU9250 I2C/SPI connection from DIP switch. SPI is much more faster than I2C for the **BH Pilot**-Raspberry Pi bundle, especially when we are running ardupilot.

- Added a 256KB EEPROM CAT24C256. It features a 64−byte page write buffer and supports the Standard (100 kHz), Fast (400 kHz) and Fast−Plus (1 MHz) I2C protocol.

- Added DS1339 RTC and a rechargeable battery MS621FE. This could compensate Raspberry Pi lacking of hardware RTC.

You see, **BH** is getting better and better!