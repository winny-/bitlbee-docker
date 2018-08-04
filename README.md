This is a modified version of
[vanityshed/bitlbee-alpine-plugins](https://hub.docker.com/r/vanityshed/bitlbee-alpine-plugins/)
with XMPP, ICQ, and Bonjour support included.

## BitlBee on Alpine with Plugins
![Docker Pulls](https://img.shields.io/docker/pulls/winny314/bitlbee-docker-plugins-xmpp.svg)
![Docker Stars](https://img.shields.io/docker/stars/winny314/bitlbee-docker-plugins-xmpp.svg)

Minimal build of latest BitlBee on latest Alpine with latest plugins for:
* [Discord](https://github.com/sm00th/bitlbee-discord)
* [Facebook](https://github.com/jgeboski/bitlbee-facebook)
* [Skype](https://github.com/EionRobb/skype4pidgin)
* [Slack](https://github.com/dylex/slack-libpurple)
* [Steam](https://github.com/bitlbee/bitlbee-steam)
* [Telegram](https://github.com/majn/telegram-purple)

## Typical Usage

For configuration persistance, `/opt/dockerdata/bitlbee` should be present on the host with sufficient permissions.

##### Using Docker CLI
```
docker run -d --name bitlbee --restart=always \
-v /opt/dockerdata/bitlbee:/bitlbee-data:rw \
-v /etc/localtime:/etc/localtime:ro \
-p 6667:6667 \
winny314/bitlbee-docker-plugins-xmpp
```

##### Using Docker Compose
```
docker-compose up -d
```
