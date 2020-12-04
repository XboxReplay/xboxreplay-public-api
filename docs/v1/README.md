# XboxReplay - Public API (v1)

### Public documentation

-   [Players](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/players.md)
-   [Game DVR](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/game-dvr.md)
-   [Search](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/search.md)
-   [Games](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/games.md)
-   [Errors](https://github.com/XboxReplay/xboxreplay-public-api/blob/master/docs/errors.md)

### Sample call

```shell
curl 'https://api.xboxreplay.net/players/major%20nelson' \
    -H 'Authorization: XR-User-Token u={preamble};{token}'
```

### Rate limiting

-   XR-User-Token: 100 requests per hour
-   XR-Partner-Token: 5k requests per hour (may be adjusted based on your needs)

##### Returned headers

Limit not reached:

```
x-rate-limit-limit: 100
x-rate-limit-remaining: 93
x-rate-limit-reset: Sat Jun 13 2020 16:36:34 GMT+0000 (Coordinated Universal Time)
```

Limit reached:

```
retry-after: Sat Jun 13 2020 16:36:34 GMT+0000 (Coordinated Universal Time)
x-rate-limit-limit: 100
x-rate-limit-remaining: 0
x-rate-limit-reset: Sat Jun 13 2020 16:36:34 GMT+0000 (Coordinated Universal Time)
```

### Token request

Feel free to contact us on Twitter [@XboxReplayNet](https://twitter.com/XboxReplayNet) or by email at [api@xboxreplay.net](mailto:api@xboxreplay.net).

##### Thanks for using XboxReplay!
