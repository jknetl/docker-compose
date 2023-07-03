ARG NEXTCLOUD_VERSION=latest
FROM nextcloud:$NEXTCLOUD_VERSION

RUN apk update && apk add ffmpeg && rm -rf /var/cache/apk/*
