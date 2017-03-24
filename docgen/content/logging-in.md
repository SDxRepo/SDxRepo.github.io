---
weight: 21
title: Logging In

---


# Logging In

## Authenticate User

```shell
curl -X POST
  -H "Accept: application/json"
  -H "Content-Type: application/json" 
  http://<host>/api/authenticate-user -d "<BODY>"
```
> Body structure:

```json
{ 
  "email":"*email*",
  "password":"*password*"
}
```
> The above command returns JSON structured like this:

```json
{
  "user": {
    "email": "*email",
    "userId": "*userId",
    "firstName": "*firstName",
    "lastName": "*lastName",
    "middleName": "*middleName",
    "sportId": "*sportId"
  },
  "authToken": "*authToken"
}
```

Log in to obtain a token (`authToken` field in the response object) and use this in the header for subsequent requests to `s-api` endpoints.

E.g. `-H Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn`

### HTTP Request

`POST http://<host>/api/authenticate-user`

## Forgot Password

```shell
curl -X POST
  -H "Accept: application/json"
  -H "Content-Type: application/json" 
  http://<host>/api/forgot-password -d "<BODY>"
```
> Body structure:

```json
{ 
  "email":"*email*"
}
```

User will recieve an email with the code once the call returns

### HTTP Request

`POST http://<host>/api/forgot-password`

## Update Password

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/api/change-password -d "<BODY>"
```
> Body structure:

```json
{ 
  "userId":"*userId",
  "currentPassword":"*currentPassword",
  "newPassword":"*newPassword"
}
```

Updates the password for a given user

<aside class="notice">
Be sure to place the authorization header even though this isn't an `s-api` endpoint.
</aside>

### HTTP Request

`POST http://<host>/api/change-password`

## Log Out

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/logout -d "<BODY>"
```
> Body structure:

```json
{ 
  "userId":"*userId"
}
```

Logs the user out (invalidates the Bearer token)

### HTTP Request

`POST http://<host>/s-api/logout`