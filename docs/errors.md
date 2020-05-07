# XboxReplay - Errors

Invalid calls will result to defined response scheme with a non-2XX HTTP response status code.

### Scheme
```
{
   "statusCode": number;
   "error":" string;
   "message": string;
}
```

### Sample errors
```json
{
   "statusCode": 401,
   "error": "Unauthorized",
   "message": "Missing credentials."
}
```

```json
{
   "statusCode": 403,
   "error": "Forbidden",
   "message": "Invalid credentials."
}
```

```json
{
   "statusCode": 404,
   "error": "Not Found",
   "message": "Player not found."
}
```

```json
{
   "statusCode": 500,
   "error": "Internal error",
   "message": "Something went wrong..."
}
```
