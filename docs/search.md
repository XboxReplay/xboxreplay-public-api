# XboxReplay - Search

### Methods
* GET - /search/game-dvr
* GET - /search/games

### Game DVR Search
Returns latest Game DVR items for a targeted player.

##### Query parameters
* target: {string} Required - Game DVR items type [screenshots | clips]
* gamertag: {string} Required - Targeted player's gamertag
* game_id: {string|integer} Optional - Targeted Game ID (May contains multiple IDs separated by commas)
* limit: {integer} Optional - Max items to be returned - Default: 25 - Max: 100

##### Sample calls
```shell
curl 'https://api.xboxreplay.net/search/game-dvr?target=screenshots&gamertag=MR4KUPSCALER&limit=1' \
    -H 'Authorization: [type] [value]'
```

```shell
curl 'https://api.xboxreplay.net/search/game-dvr?target=screenshots&gamertag=major%20nelson&game_id=175227487&limit=1' \
    -H 'Authorization: [type] [value]'
```

##### Sample responses
```json
{
    "data": [
        {
            "id": "ffbe1a9d-6c83-4fa4-9e88-db1d74c98651",
            "type": "screenshot",
            "author": {
                "gamertag": "MR4KUPSCALER",
                "gamerpic": "https://images-eds-ssl.xboxlive.com/image?url=wHwbXKif8cus8csoZ03RWwcxuUQ9WVT6xh5XaeeZD02wEfGZeuD.XMoGFVYkwHDqjE1TMOY534xB7iFT6llOMdb70jgtpdiJQNgLtYutV8bdbyiNw5Om5.khTiIkfSMNGbOsNfWtrecYJJ5QGsUrPbml_WxKMU1Xx.Emo6si4Gk-&format=png"
            },
            "game": {
                "id": 374923716,
                "name": "Gears 5"
            },
            "thumbnail_urls": {
                "small": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG",
                "large": "https://screenshotscontent-t4001.xboxlive.com/xuid-2584878536129841-public/1f8225be-38a7-47e9-9952-7aecbf18285c_Thumbnail.PNG"
            },
            "metadata": {
                "views": 8
            },
            "download_urls": {
                "source": "https://api.xboxreplay.net/ugc-files/xuid-2533274802223855/ffbe1a9d-6c83-4fa4-9e88-db1d74c98651/screenshot.png",
                "hdr": "https://api.xboxreplay.net/ugc-files/xuid-2533274802223855/ffbe1a9d-6c83-4fa4-9e88-db1d74c98651/screenshot.jxr"
            },
            "uploaded_at": "2019-09-07T00:10:39.000Z"
        }
    ]
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
    ]
}
```

### Games search

##### Query parameters
* id: {number} Required - Targeted game ID
* lang: {string} Optional - Desired language [en-us | fr-fr] - Default: en-us

##### Warning
Name, description and metadata (such as rating system / value) may vary based on the specified language.

##### Sample call
```shell
curl 'https://api.xboxreplay.net/search/games?id=770775860&lang=en-us' \
    -H 'Authorization: [type] [value]'
```

##### Sample response
```json
{
    "id": 770775860,
    "name": "RESIDENT EVIL 3",
    "description": "Jill Valentine is one of the last remaining people in Raccoon City to witness the atrocities Umbrella performed. To stop her, Umbrella unleashes their ultimate secret weapon; Nemesis!",
    "image_urls": {
        "boxart": "https://store-images.s-microsoft.com/image/apps.4880.71880157815410720.768ba6e5-793f-45af-8f98-a14bc261e1c1.5634c02b-d53f-43e1-b132-de624b29bac2",
        "hero": "https://store-images.s-microsoft.com/image/apps.33165.71880157815410720.768ba6e5-793f-45af-8f98-a14bc261e1c1.a913127d-06dc-4f3d-9409-d7416e6bf0f7"
    },
    "metadata": {
        "min_age": 18,
        "game_pass": false,
        "publisher": "CAPCOM CO., LTD.",
        "developer": "CAPCOM CO., LTD.",
        "release_date": "2019-12-12T00:59:40.7409122Z",
        "rating": {
            "system": "ESRB",
            "value": "ESRB:18"
        },
        "devices": [
            "XboxOne"
        ]
    },
    "updated_at":"2020-05-10T17:14:00.242Z"
}
```
