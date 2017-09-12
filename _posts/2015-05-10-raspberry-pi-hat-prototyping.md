---
ID: 540
post_title: Raspberry Pi HAT prototyping
author: bithollow
post_excerpt: ""
layout: post
permalink: >
  https://bithollow.com/raspberry-pi-hat-prototyping/
published: true
post_date: 2015-05-10 07:11:09
---
Our hobbies come to a new level, we want to design a HAT for Raspberry Pi, which includes 10 DoF, PWM I/O, GNSS, RTC and various LEDs, extension ports.

This HAT can be used as the compliment to Raspberry Pi, so it could act as an autopilot who is able to pilot drones, rovers. This will add a lot of fun to the DIYers, by using a modern Linux, making their dreamed little projects.

We plan to support it in the official [Ardupilot](http://ardupilot.org) software stack, so as to [ROS](http://ros.org). However, Rome was not built within a day.

Let us making a prototype to help realizing our idea. For the 10 DoF, [GY-86](http://www.ebay.com/itm/GY-86-MS5611-HMC5883L-MPU6050-MWC-Flight-Control-Sensor-Module-10DOF-/253074571047?hash=item3aec6b7f27:g:d9gAAOSwjTlZgXH9) is a good choice. It has MPU6050 (accel/gypo), HMC5883L (mag), MS5611 (baro), interfaces with I2C; For the PWM output, PCA9685 can fulfill the needs, but we can't find a break-out board which can be easily connected to Raspberry Pi, seems we should try a bread board; For the PWM input, maybe sampling GPIO states of Raspberry Pi could do it; Ublox NEO M8N is our preferred GNSS, affordable cost with good performance.

Get the hands dirty!