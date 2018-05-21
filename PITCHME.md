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

Camera --(raw file)--> encoder --(encoded file)--> Stream server(s) --(encoded file)--> Client

+++

## RTMP

Camera --(raw file)--> encoder --(encoded file)--> Origin stream server --(flv with RTMP)--> Edge stream servers --(flv with RTMP)--> Adobe Flash Player

+++

## Drawback of RTMP streaming

- Flash is fading out
- RTMP is not using 80/443 port
- Require lots of edge servers

Note:

HLS can solve the above problems

---

# What is HTTP Live Streaming?


---

# The HTML5 player framework - Video.js

---

# Customizing Video.js

---

# Demonstration
