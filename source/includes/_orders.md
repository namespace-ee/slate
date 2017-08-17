# Orders

## List Orders

> The above command returns JSON structured like this:

```json
[
  {
    "id": "ed4b1f96-caf2-4943-b314-6a4d7771d6e2",
    "url": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "customer": {},
    "language": "et",
    "state": "cart",
    "items": [
      {
        "product": "https://tickets.namespace.ee/api/products/6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4/",
        "quantity": 2,
        "unit_base": "57.50",
        "unit_vat": "11.50",
        "unit_price": "69.00",
        "vat_percent": "20"
      },
      {
        "product": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf",
        "quantity": 2,
        "unit_base": "65.83",
        "unit_vat": "13.17",
        "unit_price": "79.00",
        "vat_percent": "20"
      }
    ],
    "cart_expires_at": null,
    "checkout_expires_at": null
  }
]
```

This endpoint retrieves all the orders.

### HTTP Request

`GET https://tickets.namespace.ee/api/orders/`

## Get a Specific Order

> The above command returns JSON structured like this:

```json
{
  "id": "ed4b1f96-caf2-4943-b314-6a4d7771d6e2",
  "url": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
  "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "customer": {},
  "language": "et",
  "state": "cart",
  "items": [
    {
      "product": "https://tickets.namespace.ee/api/products/6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4/",
      "quantity": 2,
      "unit_base": "57.50",
      "unit_vat": "11.50",
      "unit_price": "69.00",
      "vat_percent": "20"
    },
    {
      "product": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf",
      "quantity": 2,
      "unit_base": "65.83",
      "unit_vat": "13.17",
      "unit_price": "79.00",
      "vat_percent": "20"
    }
  ],
  "cart_expires_at": null,
  "checkout_expires_at": null
}
```

This endpoint retrieves a specific order.

### HTTP Request

`GET https://tickets.namespace.ee/api/orders/<UUID>`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the order to retrieve

## Create a Order

> The above command returns JSON structured like this:

```json
{
  "id": "ed4b1f96-caf2-4943-b314-6a4d7771d6e2",
  "url": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
  "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "customer": {},
  "language": "et",
  "state": "cart",
  "items": [
    {
      "product": "https://tickets.namespace.ee/api/products/6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4/",
      "quantity": 2,
      "unit_base": "57.50",
      "unit_vat": "11.50",
      "unit_price": "69.00",
      "vat_percent": "20"
    },
    {
      "product": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf",
      "quantity": 2,
      "unit_base": "65.83",
      "unit_vat": "13.17",
      "unit_price": "79.00",
      "vat_percent": "20"
    }
  ],
  "cart_expires_at": null,
  "checkout_expires_at": null
}
```

This endpoint retrieves a specific order.

### HTTP Request

`POST https://tickets.namespace.ee/api/orders/`

### JSON Parameters

Parameter      | Description
-------------- | -----------
event          | The URL of the order the payment is for
items          | Array of Items for the order

### Items JSON Parameters
Parameter      | Description
-------------- | -----------
product        | The URL of the product
quantity       | Quantity of the product


## Update an Order

> The above command returns JSON structured like this:

```json
{
  "id": "ed4b1f96-caf2-4943-b314-6a4d7771d6e2",
  "url": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
  "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "customer": {},
  "language": "et",
  "state": "cart",
  "items": [
    {
      "product": "https://tickets.namespace.ee/api/products/6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4/",
      "quantity": 2,
      "unit_base": "57.50",
      "unit_vat": "11.50",
      "unit_price": "69.00",
      "vat_percent": "20"
    },
    {
      "product": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf",
      "quantity": 2,
      "unit_base": "65.83",
      "unit_vat": "13.17",
      "unit_price": "79.00",
      "vat_percent": "20"
    }
  ],
  "cart_expires_at": null,
  "checkout_expires_at": null
}
```

This endpoint creates the specified order and reserves quantities of products.

### HTTP Request

`PATCH https://tickets.namespace.ee/api/orders/<UUID>`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the order to retrieve

### JSON Parameters

Parameter      | Description
-------------- | -----------
items          | Array of Items for the order

### Items JSON Parameters
Parameter      | Description
-------------- | -----------
product        | The URL of the product
quantity       | Quantity of the product


## Checkout an Order

> The above command returns JSON structured like this:

```json
{
  "id": "ed4b1f96-caf2-4943-b314-6a4d7771d6e2",
  "url": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
  "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "customer": {},
  "language": "et",
  "state": "checkout",
  "items": [
    {
      "product": "https://tickets.namespace.ee/api/products/6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4/",
      "quantity": 2,
      "unit_base": "57.50",
      "unit_vat": "11.50",
      "unit_price": "69.00",
      "vat_percent": "20"
    },
    {
      "product": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf",
      "quantity": 2,
      "unit_base": "65.83",
      "unit_vat": "13.17",
      "unit_price": "79.00",
      "vat_percent": "20"
    }
  ],
  "cart_expires_at": null,
  "checkout_expires_at": null
}
```

This endpoint creates the specified order and reserves quantities of products.

### HTTP Request

`POST https://tickets.namespace.ee/api/orders/<UUID>/checkout/`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the order to retrieve

### JSON Parameters

An empty json dictionary {} can be passed as data for checkout request.

## Abort an Order

> The above command returns JSON structured like this:

```json
{
  "id": "ed4b1f96-caf2-4943-b314-6a4d7771d6e2",
  "url": "https://tickets.namespace.ee/api/orders/ed4b1f96-caf2-4943-b314-6a4d7771d6e2/",
  "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "customer": {},
  "language": "et",
  "state": "cart",
  "items": [],
  "cart_expires_at": null,
  "checkout_expires_at": null
}
```

This endpoint aborts the specified order and releases quantities of products.

### HTTP Request

`POST https://tickets.namespace.ee/api/orders/<UUID>/`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the order to retrieve

### JSON Parameters

An empty items array {} should be passed as data for abort request.

## Send tickets by email

> The above command should send JSON structured like this:

```json
{
  "email": "testuser@awesome-festival.ee"
}
```

This endpoint sends emails with the ticket PDF's.

### HTTP Request

`POST https://tickets.namespace.ee/api/orders/<UUID>/email/`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the order to retrieve

### JSON Parameters

Parameter      | Description
-------------- | -----------
email          | Email where the tickets should be sent to
