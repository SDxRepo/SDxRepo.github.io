---
weight: 10
title: SportDx API Reference
---

# Introduction

Welcome to the SportDx API! Discover, Collaborate, and get it done!

### All calls starting with `s-api` require authentication token in the header

# Generic API calls

## Global Config

```shell
curl -i
  -H "Accept: application/json"
  -H "Content-Type: application/json" 
  http://<host>/api/global-config
```

Get Global Config

### HTTP Request

`GET http://<host>/api/global-config`

<aside class="notice">
No need for headers here
</aside>

## View File

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/view-file -d "<BODY>"
```
> Body structure:

```json
{ 
  "path":"sportx.log, sportx.err.log"
}
```

View a file

### HTTP Request

POST `http://<host>/s-api/view-file`
