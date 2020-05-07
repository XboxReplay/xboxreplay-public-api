# XboxReplay - Players information

### Sample usage
```
curl 'https://api.xboxreplay.net/players/major%20nelson' \
    -H 'Authorization: [type] [value]'
```

### Sample response
```
{
   "gamertag": "Major Nelson",
   "gamerpic" :"https://images-eds-ssl.xboxlive.com/image?url=wHwbXKif8cus8csoZ03RWwcxuUQ9WVT6xh5XaeeZD02wEfGZeuD.XMoGFVYkwHDqVbTLNl4uG5GNlAu6C3Nxw2PMhnEdJ.tx.hq4uEXu6o1HG6BQpsWdC0fG4OXmAbbCBSXId4EtCKrSkjvcxYDKw16NCNi.s5KQax77.1h7OCM-&format=png",
   "colors": {
      "primary": "#eb4910",
      "secondary": "#692015",
      "tertiary": "#ab2d11"
   }
}
```

### Sample error
```json
{
   "statusCode": 404,
   "error": "Not Found",
   "message": "Player not found."
}
```
