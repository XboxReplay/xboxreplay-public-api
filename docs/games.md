# XboxReplay - Games

### Methods
* GET - /games
* GET - /games/{id}

### Games
Returns synchronized games on XboxReplay.

##### Query parameters
* count: {number} Optional - Desired count - Default: 36 - Max: 100
* offset: {number} Optional - Desired offset - Default: 0
* sort: {string} Optional - Desired sort [asc | desc] - Default: asc
* lang: {string} Optional - Desired language [en-us | fr-fr] - Default: en-us
* filter: {string} Optional - Desired filter [game-pass]
* search: {string} Optional - Search query

##### Warning
Games and their informations may vary based on the specified language.

##### Sample call
```shell
curl 'https://api.xboxreplay.net/games?count=1&search=resident%20evil%203&lang=en-us' \
    -H 'Authorization: [type] [value]'
```

##### Sample response
```json
{
    "data": [
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
    ],
    "additional": {
        "total": 2
    }
}
```

### Game ID
Returns synchronized game on XboxReplay.

##### Query parameters
* lang: {string} Optional - Desired language [en-us | fr-fr] - Default: en-us

##### Warning
Name, description and metadata (such as rating system / value) may vary based on the specified language.

##### Sample call
```shell
curl 'https://api.xboxreplay.net/games/770775860' \
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
