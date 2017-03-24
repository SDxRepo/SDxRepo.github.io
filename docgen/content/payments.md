---
weight: 50
title: Payments

---

# Payments

## Get Credit Card Details

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/get-credit-card-details -d "<BODY>"
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
  "cardData":
  [
    {
      "cardNumber": "*cardNumber",
      "cardType": "*cardType",
      "cardCode": "*cardCode",
    }, 
    {
      "cardNumber": "*cardNumber",
      "cardType": "*cardType",
      "cardCode": "*cardCode",
    },
    ...
  ],
  "coinBalance": "*coinBalance",
  "accountBalance": "*accountBalance"
}
```

Get some non-sensitive credit card details

### HTTP Request

POST `http://<host>/s-api/get-credit-card-details`

<aside class="warning">
We do NOT store sensitive data. `cardNumber` would be just the last 4 digits.
</aside>