hubot-mattermost
================

## Overview
scratch images "hubot-mattermost" build on docker

## Usage
```
$ docker run -it -p 8080:8080 -e MATTERMOST_TOKEN=“<Mattermost Outgoing Webhooks Token>” \
  -e MATTERMOST_INCOME_URL=“<Matttermost Incoming Webhooks URL>” \
  -d rsakao/hubot-mattermost
```
