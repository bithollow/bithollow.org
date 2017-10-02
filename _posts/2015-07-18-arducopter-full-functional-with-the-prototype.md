---
ID: 581
post_title: >
  Arducopter full functional with the
  prototype
author: bithollow
post_excerpt: ""
layout: post
permalink: >
  https://bithollow.com/arducopter-full-functional-with-the-prototype/
published: true
post_date: 2015-07-18 19:47:39
---
The ardupilot software is almost done by the code, there are existing support for MPU6050, MS5611, HMC5883L and Ublox serial GNSS. What I did was to add a new "board" in the build system of ardupilot, specify the drivers the prototype that depends on.



<blockquote>After clean the code, and make a "decent" board, I guess we can merge the source code into upstream, so we could announce the official support of ardupilot.</blockquote>

### Prototype with GPS ###

Bought a Ublox NEO 6 GPS, so it could switch to almost all the ardupilot flight modes. Loiter mode looks quite stable in the wind.

[bithollow_video locale="China" url="https://v.youku.com/v_show/id_XMTI4NzYwNzkyNA==.html"]

[bithollow_video locale="Global" url="https://vimeo.com/139907305"]

### RTL, return to land, very precise, error less in one feet ###

Flying loiter mode for a while, switch to RTL, more than expected!

[bithollow_video locale="China" url="https://v.youku.com/v_show/id_XMTI4NzYwOTk2NA==.html"]

[bithollow_video locale="Global" url="https://vimeo.com/139907468"]