---
weight: 22
title: User Management

---


# User Management

## Get User Portfolio Status

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/get-user-portfolio-status -d "<BODY>"
```
> Body structure:

```json
{ 
  "user":"*user"
}
```

Get the current user's portfolio status

### HTTP Request

POST `http://<host>/s-api/get-user-portfolio-status`

## Get User's Watchlist players

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/watchlist-get-player-list -d "<BODY>"
```
> Body structure:

```json
{ 
  "user":"*user"
}
```

Get the current user's watchlist players

### HTTP Request

POST `http://<host>/s-api/watchlist-get-player-list`

## Add player to User's Watchlist

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/watchlist-add-player -d "<BODY>"
```
> Body structure:

```json
{
  "symbol":"*symbol",
  "user":"*user",
  "entryTime":"*entryTime",
  "endTime":"*endTime"
}
```

> entryTime and endTime format is: "dd-MMM-yy" e.g. "03-JAN-17"

Add a player to the current user's watchlist

### HTTP Request

POST `http://<host>/s-api/watchlist-add-player`

## Remove player from User's Watchlist

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/watchlist-remove-player -d "<BODY>"
```
> Body structure:

```json
{
  "symbol":"*symbol",
  "user":"*user"
}
```

Remove the a player from the current user's watchlist

### HTTP Request

POST `http://<host>/s-api/watchlist-remove-player`

## Get Profile Picture

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/get-profile-picture -d "<BODY>"
```
> Body structure:

```json
{
  "userId":"*userId"
}
```
> The above command returns JSON structured like this:

```json
{
  "profilePicture":"*base64String"
}
```

Get profile picture

### HTTP Request

POST `http://<host>/s-api/get-profile-picture`

## Update Profile Picture

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/update-profile-picture -d "<BODY>"
```
> Body structure:

```json
{
  "userId":"*userId",
  "profilePicture":"*base64String"
}
```

Update profile picture

### HTTP Request

POST `http://<host>/s-api/update-profile-picture

## Get Profile

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/get-profile -d "<BODY>"
```
> Body structure:

```json
{
  "userId":"*userId"
}
```
> The above command returns JSON structured like this:

```json
{
  "userId":"*userId",
  "firstName":"*firstName",
  "middleName":"*middleName",
  "lastName":"*lastName",
  "address1":"*address1",
  "address2":"*address2",
  "address3":"*address3",
  "city":"*city",
  "state":"*state",
  "county":"*county",
  "postalCode":"*postalCode",
  "cellPhone":"*cellPhone",
  "homePhone":"*homePhone",
  "busPhone":"*busPhone"
}
```

Get basic metadata for a given user

### HTTP Request

POST `http://<host>/s-api/get-profile`

## Update Profile

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/update-profile -d "<BODY>"
```
> Body structure:

```json
{
  "userId":"*userId",
  "firstName":"*firstName",
  "middleName":"*middleName",
  "lastName":"*lastName",
  "address1":"*address1",
  "address2":"*address2",
  "address3":"*address3",
  "city":"*city",
  "state":"*state",
  "county":"*county",
  "postalCode":"*postalCode",
  "cellPhone":"*cellPhone",
  "homePhone":"*homePhone",
  "busPhone":"*busPhone"
}
```

Get basic metadata for a given user

### HTTP Request

POST `http://<host>/s-api/update-profile`

<aside class="notice">
All parameters optional except for userId
</aside>