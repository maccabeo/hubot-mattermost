# hubot-mattermost

## Overview
hubot-mattermost is Hubot mattermost adapter included docker image.

## Usage

### Docker run
```
$ docker run -it -d -p 8080:8080 \
  -e MATTERMOST_TOKEN='<Mattermost Outgoing Webhooks Token>' \
  -e MATTERMOST_INCOME_URL='<Matttermost Incoming Webhooks URL>' \
  --name matterbot rsakao/hubot-mattermost
```
#### Example enviroment
`<Mattermost Outgoing Webhooks Token>` -> `oqwx9d4khjra8cw3zbis1w6fqy`  
`<Matttermost Incoming Webhooks URL>` -> `http://<your mattermost instance>:<port>/hooks/ncwc66caqf8d7c4gnqby1196qo`

### Custom enviroment Docker run
```
$ docker run -it -d -p 8080:8080 \
  -e MATTERMOST_TOKEN='oqwx9d4khjra8cw3zbis1w6fqy' \
  -e MATTERMOST_INCOME_URL='http://matterbot:8065/hooks/ncwc66caqf8d7c4gnqby1196qo' \
  -e MATTERMOST_ENDPOINT='/hubot/incoming'
  -e MATTERMOST_HUBOT_USERNAME='matterbot'
  -e MATTERMOST_CHANNEL='town-square'
  -e MATTERMOST_ICON_URL='https://s3-eu-west-1.amazonaws.com/renanvicente/toy13.png'
  -e MATTERMOST_SELFSIGNED_CERT=true
  --name matterbot rsakao/hubot-mattermost
```

### Environment variables
```
MATTERMOST_TOKEN
MATTERMOST_INCOME_URL
MATTERMOST_ENDPOINT
MATTERMOST_HUBOT_USERNAME
MATTERMOST_CHANNEL
MATTERMOST_ICON_URL
MATTERMOST_SELFSIGNED_CERT
```
enviroment detail [renanvicente/hubot-mattermost](https://github.com/renanvicente/hubot-mattermost/blob/master/README.md#environment-variables)
