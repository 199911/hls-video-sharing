# Live demo

## Prerequisite

- Docker
    - brew cask install docker
- OBS
    - brew cask install obs
    - Streaming config
        - server url: rtmp://127.0.0.1/show
        - stream key: hkoscon
        - stream link: http://localhost:8080/hls/hkoscon.m3u8

## Set up

- docker build -t nginx-rtmp-2-hls .
- docker run -d -p 1935:1935 -p 8080:8080 --name nginx-rtmp-2-hls nginx-rtmp-2-hls

## Reference

- [nginx-rtmp docker image](https://hub.docker.com/r/tiangolo/nginx-rtmp/)
- [nginx-rtmp to hls config](https://docs.peer5.com/guides/setting-up-hls-live-streaming-server-using-nginx/)
