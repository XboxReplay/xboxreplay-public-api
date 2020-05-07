# XboxReplay - Game DVR

### Methods
* GET - /players/{gamertag}/{target}
* GET - /players/{gamertag}/{target}/{id}
* GET - /players/{gamertag}/{target}/latest

### Notice
Please note that an asynchronous process is started each 15 minutes to retrieve all files for the targeted player. If player's files aren't available on our database the returned `data` node will be equal to `null`. Please refer to the `pull` node to follow the pulling progress. Of course, this step isn't longer required once files are available.

### Game DVR items
Returns all Game DVR items for a targeted player.

##### Sample call
```shell
curl 'https://api.xboxreplay.net/players/major%20nelson/screenshots' \
    -H 'Authorization: [type] [value]'
```

##### Sample responses
```json
{
    "data": null,
    "additional": {
        "total": 0
    },
    "pull": {
        "status": "waiting",
        "updated_at": "2020-05-07T11:28:44.718Z"
    }
}
```

```json
{
    "data": null,
    "additional": {
        "total": 0
    },
    "pull": {
        "status": "started",
        "updated_at": "2020-05-07T11:28:45.111Z"
    }
}
```

```json
{
    "data": null,
    "additional": {
        "total": 0
    },
    "pull": {
        "status": "error",
        "updated_at": "2020-05-07T11:28:45.931Z"
    }
}
```

```json
{
    "data": [],
    "additional": {
        "total": 0
    },
    "pull": {
        "status": "ended",
        "updated_at": "2020-05-07T11:28:45.946Z"
    }
}
```

```json
{
    "data": [
        {
            "id": "1f8225be-38a7-47e9-9952-7aecbf18285c",
            "type": "screenshot",
            "author": {
                "gamertag": "Major Nelson",
                "gamerpic": "https://images-eds-ssl.xboxlive.com/image?url=wHwbXKif8cus8csoZ03RWwcxuUQ9WVT6xh5XaeeZD02wEfGZeuD.XMoGFVYkwHDqVbTLNl4uG5GNlAu6C3Nxw2PMhnEdJ.tx.hq4uEXu6o1HG6BQpsWdC0fG4OXmAbbCBSXId4EtCKrSkjvcxYDKw16NCNi.s5KQax77.1h7OCM-&format=png"
            },
            "game": {
                "id": 175227487,
                "name": "Apex Legends™"
            },
            "thumbnail_urls": {
                "small": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG",
                "large": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG"
            },
            "metadata": {
                "views": 3082
            },
            "download_urls": {
                "source": "https://api.xboxreplay.net/ugc-files/xuid-2584878536129841/1f8225be-38a7-47e9-9952-7aecbf18285c/screenshot.png",
            },
            "uploaded_at": "2019-11-30T03:37:18.000Z"
        }
    ],
    "additional": {
        "total": 1
    },
    "pull": {
        "status": "ended",
        "updated_at": "2020-05-07T11:28:45.946Z"
    }
}
```

### Game DVR item
Returns a specified Game DVR item for a targeted player.

##### Sample call
```shell
curl 'https://api.xboxreplay.net/players/major%20nelson/screenshots/1f8225be-38a7-47e9-9952-7aecbf18285c' \
    -H 'Authorization: [type] [value]'
```

##### Sample response
```json
{
    "data": {
        "id": "1f8225be-38a7-47e9-9952-7aecbf18285c",
        "type": "screenshot",
        "author": {
            "gamertag": "Major Nelson",
            "gamerpic": "https://images-eds-ssl.xboxlive.com/image?url=wHwbXKif8cus8csoZ03RWwcxuUQ9WVT6xh5XaeeZD02wEfGZeuD.XMoGFVYkwHDqVbTLNl4uG5GNlAu6C3Nxw2PMhnEdJ.tx.hq4uEXu6o1HG6BQpsWdC0fG4OXmAbbCBSXId4EtCKrSkjvcxYDKw16NCNi.s5KQax77.1h7OCM-&format=png"
        },
        "game": {
            "id": 175227487,
            "name": "Apex Legends™"
        },
        "thumbnail_urls": {
            "small": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG",
            "large": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG"
        },
        "metadata": {
            "views": 3082
        },
        "download_urls": {
            "source": "https://api.xboxreplay.net/ugc-files/xuid-2584878536129841/1f8225be-38a7-47e9-9952-7aecbf18285c/screenshot.png",
        },
        "uploaded_at": "2019-11-30T03:37:18.000Z"
    },
    "additional": {
        "total": 1
    },
    "pull": {
        "status": "ended",
        "updated_at": "2020-05-07T11:28:45.946Z"
    }
}
```

### Game DVR latest item
Returns latest Game DVR item for a targeted player.

##### Sample call
```shell
curl 'https://api.xboxreplay.net/players/major%20nelson/screenshots/latest' \
    -H 'Authorization: [type] [value]'
```

##### Sample response
```json
{
    "data": {
        "id": "1f8225be-38a7-47e9-9952-7aecbf18285c",
        "type": "screenshot",
        "author": {
            "gamertag": "Major Nelson",
            "gamerpic": "https://images-eds-ssl.xboxlive.com/image?url=wHwbXKif8cus8csoZ03RWwcxuUQ9WVT6xh5XaeeZD02wEfGZeuD.XMoGFVYkwHDqVbTLNl4uG5GNlAu6C3Nxw2PMhnEdJ.tx.hq4uEXu6o1HG6BQpsWdC0fG4OXmAbbCBSXId4EtCKrSkjvcxYDKw16NCNi.s5KQax77.1h7OCM-&format=png"
        },
        "game": {
            "id": 175227487,
            "name": "Apex Legends™"
        },
        "thumbnail_urls": {
            "small": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG",
            "large": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG"
        },
        "metadata": {
            "views": 3082
        },
        "download_urls": {
            "source": "https://api.xboxreplay.net/ugc-files/xuid-2584878536129841/1f8225be-38a7-47e9-9952-7aecbf18285c/screenshot.png",
        },
        "uploaded_at": "2019-11-30T03:37:18.000Z"
    },
    "additional": {
        "total": 1
    },
    "pull": {
        "status": "ended",
        "updated_at": "2020-05-07T11:28:45.946Z"
    }
}
```
