# XboxReplay - Public API
Take the advantage of the XboxReplay API for you own use, and for **free**!

### Documentation
* [Players](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/players.md)
* [Game DVR](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/game-dvr.md)
* [Search](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/search.md)
* [Errors](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/errors.md)

### Sample call
```shell
curl 'https://api.xboxreplay.net/players/major%20nelson' \
    -H 'Authorization: XR-User-Token u={preamble};{token}'
```

### Rate limiting
* XR-User-Token: 100 requests per hour
* XR-Partner-Token: 5k requests per hour

### Token request
Feel free to contact us on Twitter [@XboxReplayNet](https://twitter.com/XboxReplayNet) or by email at [api@xboxreplay.net](mailto:api@xboxreplay.net).

##### Thanks for using XboxReplay!
