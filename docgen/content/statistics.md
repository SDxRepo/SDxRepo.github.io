---
weight: 30
title: Statistics

---

# Statistics

## Search Player

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/search-player -d "<BODY>"
```
> Body structure:

```json
{
    "searchText":"*searchText",
    [
        "sportId":"*sportId",
        "teamName":"*teamName"
    ]
}
```

Search for a player in the exchange

### HTTP Request

POST `http://<host>/s-api/search-player`

## Trending

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/trending -d "<BODY>"
```
> Body structure:

```json
{
    "sportId":"*sportId"
}
```

Get the currently trending players for a given sport

### HTTP Request

POST `http://<host>/s-api/trending`

## Gainers

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/gainers -d "<BODY>"
```
> Body structure:

```json
{
    "sportId":"*sportId"
}
```

Get the current gainers for a given sport

### HTTP Request

POST `http://<host>/s-api/gainers`

## Losers

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/losers -d "<BODY>"
```
> Body structure:

```json
{
    "sportId":"*sportId"
}
```

Get the current losers for a given sport

### HTTP Request

POST `http://<host>/s-api/losers`