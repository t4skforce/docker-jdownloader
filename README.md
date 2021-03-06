# JDownloader 2 Docker

[![](https://images.microbadger.com/badges/image/t4skforce/docker-jdownloader.svg)](http://microbadger.com/images/t4skforce/docker-jdownloader "Get your own image badge on microbadger.com") [![](https://img.shields.io/docker/cloud/automated/t4skforce/docker-jdownloader)](https://cloud.docker.com/repository/docker/t4skforce/docker-jdownloader) [![](https://images.microbadger.com/badges/version/t4skforce/docker-jdownloader.svg)](http://microbadger.com/images/t4skforce/docker-jdownloader "Get your own version badge on microbadger.com") [![](https://img.shields.io/docker/pulls/t4skforce/docker-jdownloader.svg)](https://cloud.docker.com/repository/docker/t4skforce/docker-jdownloader) [![](https://img.shields.io/docker/stars/t4skforce/docker-jdownloader.svg)](https://cloud.docker.com/repository/docker/t4skforce/docker-jdownloader) [![](https://img.shields.io/github/last-commit/t4skforce/docker-jdownloader.svg)](https://github.com/t4skforce/docker-jdownloader) [![](https://img.shields.io/maintenance/yes/2020.svg)](https://github.com/t4skforce/docker-jdownloader) [![](https://img.shields.io/github/issues-raw/t4skforce/docker-jdownloader.svg)](https://github.com/t4skforce/docker-jdownloader/issues) [![](https://img.shields.io/github/issues-pr-raw/t4skforce/docker-jdownloader.svg)](https://github.com/t4skforce/docker-jdownloader/pulls)

Full JDownloader install in docker container with remote access via noVNC web interface

support of env variabls:
- PUID=1000 default
- PGID=1000 default

Optional Basic Auth
- APP_USERNAME=
- APP_PASSWORD=

Optional Server Ports
- HTTP_PORT=80 default
- HTTPS_PORT=443 default

Optional Server Name
- SERVER_NAME=Hostname used for SSL certificate

exposes HTTP_PORT -> redirect -> HTTPS_PORT

autogenerated ssl certificate

## Sceenshots
<img src="https://github.com/t4skforce/docker-jdownloader/blob/master/screenshots/noVNC-Chromium_000.png?raw=true" width=1024 />
<img src="https://github.com/t4skforce/docker-jdownloader/blob/master/screenshots/JDownloader-noVNC-Chromium_001.png?raw=true" width=1024 />
<img src="https://github.com/t4skforce/docker-jdownloader/blob/master/screenshots/JDownloader-noVNC-Chromium_002.png?raw=true" width=1024 />
<img src="https://github.com/t4skforce/docker-jdownloader/blob/master/screenshots/JDownloader-noVNC-Chromium_003.png?raw=true " width=1024 />

## start
```
docker run --name docker-jdownloader -it -p 8181:8181 -p 4443:4443 -v ~/config:/data:rw -v ~/Downloads:/data/Downloads:rw -e HTTP_PORT=8181 -e HTTPS_PORT=4443 --rm t4skforce/docker-jdownloader:latest
```
