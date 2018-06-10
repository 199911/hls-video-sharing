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
- Ngrok (Optional)
    - Allow public network access your localhost stream

## Set up

- `cd <project directory>`
- `yarn install`
- `docker build -t nginx-rtmp-2-hls .`
- `docker run -d -p 1935:1935 -p 8080:8080 --name nginx-rtmp-2-hls nginx-rtmp-2-hls`
- Config and start your stream with OBS
- `python -m SimpleHTTPServer`
- Open the Video.js player in http://localhost:8000

## Set up public access

- ngrok http 8080
- Remove the local stream in index.html
- Update the ngrok stream in index.html
- Push the changes to Github
- Open your player on Github page

## Reference

- [nginx-rtmp docker image](https://hub.docker.com/r/tiangolo/nginx-rtmp/)
- [nginx-rtmp to hls config](https://docs.peer5.com/guides/setting-up-hls-live-streaming-server-using-nginx/)
