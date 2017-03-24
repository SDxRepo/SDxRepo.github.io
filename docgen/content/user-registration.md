---
weight: 20
title: User Registration

---

# User Registration

## Register a new user

```shell
curl -X POST
  -H "Accept: application/json"
  -H "Content-Type: application/json" 
  http://<host>/api/register-user -d "<BODY>"
```
> Body structure:

```json
{ 
  "email":"*email*",
  "password":"*password*",
  "cellPhone":"*cellPhone*" 
}
```

Register a new user to the app.

### HTTP Request

`POST http://<host>/api/register-user`

Password requirements:

- `2 uppercase letters`
- `1 special case letter`
- `2 digits`
- `3 lowercase letters`
- `length 8 - 16`

<aside class="notice">
You will receieve an email with a code once you finish this call
</aside>

## Confirm Registration

```shell
curl -X POST
  -H "Accept: application/json"
  -H "Content-Type: application/json" 
  http://<host>/api/registration-confirm -d "<BODY>"
```
> Body structure:

```json
{ 
  "email":"*email*",
  "password":"*password*",
  "code":"*code*" 
}
```

Take the code that was sent in the email and pass it in.

### HTTP Request

`POST http://<host>/api/registration-confirm`

<aside class="notice">
The code will be valid for 1 day
</aside>