# Video.js with HLS

HTTP Live Streaming with Opensource HTML5 video player

##### Sunday Ku

+++

# Agenda

- Live streaming data flow
- What is HTTP Live Streaming?
- The HTML5 player framework - Video.js
- Customizing Video.js
- Demonstration

---

# Live streaming data flow

Live streaming: Simultaneously record and broadcast video

+++

## In general

Recorder --(raw file)--> encoder --(encoded file)--> Stream server(s) --(encoded file)--> Client

Note:

We focus on the section of Stream servers and Clients

+++

## RTMP

Recorder --(raw file)--> encoder --(encoded file)--> Origin stream server --(flv with RTMP)--> Edge stream servers --(flv with RTMP)--> Adobe Flash Player

+++

## Drawback of RTMP streaming

- Flash is fading out
- RTMP is not using 80/443 port
- Require lots of edge servers

Note:

HLS can solve the above problems
Not using 80/443 port is critical problem. As we cannot create TCP socket in browser, we cannot get resource with browser only.
Edge servers -> expensive
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

---

# Customizing Video.js

---

# Demonstration
