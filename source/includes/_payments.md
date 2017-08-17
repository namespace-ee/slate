# Payments

## Get All Payments

> The above command returns JSON structured like this:

```json
[
  {
    "order": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
    "payment_method": "https://tickets.namespace.ee/api/payment_methods/6f527b0c-9025-468d-ad6c-d7ea04105edb/",
    "external_id": "EXTERNAL_TRANSACTION_ID",
    "reference": "A31VA4HZJ2",
    "state": "confirmed",
    "amount": "138.00",
    "transaction_fee": "0.00",
    "payable": "138.00"
  }
]
```

This endpoint retrieves all payments.

### HTTP Request

`GET https://tickets.namespace.ee/api/payments/`

### Query Parameters

Parameter       | Description
--------------- | -----------
external_id     | Filter by External ID of payment
reference       | Filter by reference of payment
state           | Filter by state of payment
amount          | Filter by amount of payment
transaction_fee | Filter by transaction fee amount of payment
payable         | Filter by payable boolean

## Get a Specific Payment

> The above command returns JSON structured like this:

```json
{
  "order": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
  "payment_method": "https://tickets.namespace.ee/api/payment_methods/6f527b0c-9025-468d-ad6c-d7ea04105edb/",
  "external_id": "EXTERNAL_TRANSACTION_ID",
  "reference": "A31VA4HZJ2",
  "state": "confirmed",
  "amount": "138.00",
  "transaction_fee": "0.00",
  "payable": "138.00"
}
```

This endpoint retrieves a specific payment.

### HTTP Request

`GET https://tickets.namespace.ee/api/payments/<UUID>`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the product group to retrieve

## Create a Payment

> The above command returns JSON structured like this:

```json
{
  "order": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
  "payment_method": "https://tickets.namespace.ee/api/payment_methods/6f527b0c-9025-468d-ad6c-d7ea04105edb/",
  "external_id": "EXTERNAL_TRANSACTION_ID",
  "reference": "A31VA4HZJ2",
  "state": "confirmed",
  "amount": "138.00",
  "transaction_fee": "0.00",
  "payable": "138.00"
}
```

This endpoint retrieves a specific payment method.

### HTTP Request

`POST https://tickets.namespace.ee/api/payments/`

### JSON Parameters

Parameter      | Description
-------------- | -----------
order          | The URL of the order the payment is for
payment_method | The URL of the payment method used for payment
external_id    | The External ID of the payment
amount         | The payment amount
