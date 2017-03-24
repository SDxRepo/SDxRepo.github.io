---
weight: 40
title: Articles

---

# Articles

## Get Articles Likes

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/get-articles-likes -d "<BODY>"
```
> Body structure:

```json
{
    "articleId":"*articleId"
}
```

Get likes for a given article

### HTTP Request

POST `http://<host>/s-api/get-articles-likes`

## Like an Article

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/add-articles-likes -d "<BODY>"
```
> Body structure:

```json
{
    "userId":"*userId",
    "articleId":"*articleId",
    "comment":"*comment",
}
```

Like an article

### HTTP Request

POST `http://<host>/s-api/add-articles-likes`

## Update Article Like

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/update-articles-likes -d "<BODY>"
```
> Body structure:

```json
{
    "userId":"*userId",
    "articleId":"*articleId",
    "isLike":"*isLike",
}
```

Updates whether a user liked the specified article

### HTTP Request

POST `http://<host>/s-api/update-articles-likes`

Parameter | Description
--------- | -----------
userId | The current user's id
articleId | The article to update
isLike | An integer: `1` for like. `0` to remove the like