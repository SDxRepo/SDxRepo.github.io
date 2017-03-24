---
weight: 30
title: The Exchange

---

# The Exchange

## Place an Order

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/place-order -d "<BODY>"
```
> Body structure:

```json
{
    "symbol":"*symbol",
    "userId":"*userId",
    "orderId":"*orderId",
    "orderType":"*orderType",
    "price":"*price",
    "quantity":"*quantity",
    "stopPrice":"*stopPrice"
}
```

Place an order in the exchange.

### HTTP Request

POST `http://<host>/s-api/place-order`

Parameter | Description
--------- | -----------
symbol | Player to place an order on
userId | current user
orderId | (leave blank)
orderType | (see below)
price | price point
quantity | amount of stock
stopPrice | the stop price

Valid `orderType`s:

 - `MarketBuy`
 - `LimitBuyDay`
 - `LimitBuyGTC`
 - `MarketSell`
 - `LimitSellDay`
 - `LimitSellGTC`
 - `StopMarketSell`
 - `StopLimitSell`
 - `TrailingStopSell`
 - `TrailingPCStopSell`

## Cancel an Order

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/cancel-order -d "<BODY>"
```
> Body structure:

```json
{
    "symbol":"*symbol",
    "userId":"*userId",
    "orderId":"*orderId",
    "orderType":"*orderType"
}
```

Cancel an order in the exchange.

### HTTP Request

POST `http://<host>/s-api/cancel-order`

Parameter | Description
--------- | -----------
symbol | Player to place an order on
userId | current user
orderId | Id of the order to cancel
orderType | (see below)

Valid `orderType`s:

 - `LimitBuyDay`
 - `LimitBuyGTC`
 - `StopMarketBuy`
 - `StopLimitBuy`
 - `TrailingStopBuy`
 - `TrailingPCStopBuy`
 - `LimitSellDay`
 - `LimitSellGTC`
 - `StopMarketSell`
 - `StopLimitSell`
 - `TrailingStopSell`
 - `TrailingPCStopSell`

## Prepare to Trade

```shell
curl -X POST 
  -H "Accept: application/json"
  -H "Content-Type: application/json"
  -H "Authorization: Bearer 3oo3irj23r9ewjf03fa309rj23leljfkfxfn"
  http://<host>/s-api/prepare-to-trade -d "<BODY>"
```
> Body structure:

```json
{
    "userId":"*userId",
    "symbol":"*symbol"
}
```

Prepare to trade for a given athlete

### HTTP Request

POST `http://<host>/s-api/prepare-to-trade`