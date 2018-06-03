# Video.js with HLS

HTTP Live Streaming with Opensource HTML5 video player

##### Sunday Ku

+++

# Agenda

- Live streaming introduction
- What is HTTP Live Streaming?
- The HTML5 player framework - Video.js
- Customizing Video.js
- Demonstration

---

# Live streaming introduction

- Context
- Live streaming terminlogy
- Live streaming architecture

+++

## Context

- Focus on video delivery
- Focus on desktop and mobile web client

Note:

Will not mention too much video recording, encoding nor transcoding
Will not discuss desktop and mobile apps

+++

## Live streaming terminlogy

- Live streaming: Simultaneously record and broadcast video
- Encode / Transcode: Convert video to other video file formats
- Bit rate: Size of the data stream when the video is playing

Note:

Encode / Transcode: It may change the quality
Encode ~= compile, convert raw video to some format can be played by common players
Transcode ~= transpile, translate from one format to another
Bit rate ~= video quality, units: kbps / mbps

+++

## Live streaming terminlogy

- Orgin stream server: "Seed" of the video delivery
- Edge stream server: Repeater of the origin stream server

Note:

Edge stream server ~= content delievery network

+++

## Live streaming architecture

![General streaming data flow](images/Live-Streaming-Data-Flow.png "General streaming data flow")

Note:

We can use any encoding between recorder and stream server, as long as your stream server support it
We focus on the section of Stream servers and Clients

+++

## Straming with Real-Time Messaging Protocol (RTMP)

![RTMP streaming data flow](images/RTMP-Data-Flow.png "RTMP streaming data flow")

Note:

Require adobe flash player to play video in flv format

+++

## Drawback of RTMP streaming

- Flash is fading out
- RTMP is not using 80/443 port
- Edge servers are expensive

Note:

Not using 80/443 port is critical problem.
- As we cannot create TCP socket in browser, we cannot get resource with browser only.
- RTMP works well in mobile and desktop apps
HLS can solve the above problems

---

# What is HTTP Live Streaming?

- Designed and implemented by Apple
- HTTP(S) based
- Media can be served by Content Delivery Network

Note:

Apple's products have native support on this protocol
We can use 80/443 port to get all resources

Mentions browser support in somewhere?

+++

Recorder --(raw file)--> encoder --(encoded file)--> Stream server --(Manifest file)--> HTML5 player with HLS support
                                                       |--(encoded media files)--> CDN --(encoded media files)--^

---

# The HTML5 player framework - Video.js

Note:

- what is it
- player structure
- browser support

---

# Customizing Video.js

Notes:

- UI components
- module
- multiplexing

---

# Demonstration

Notes:

OBS -> nginx-rtmp -> ngrok -> Github page player