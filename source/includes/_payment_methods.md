# Payment methods

## Get All Payment methods

> The above command returns JSON structured like this:

```json
[
  {
    "id": "6f527b0c-9025-468d-ad6c-d7ea04105edb",
    "url": "https://tickets.namespace.ee/api/events/6f527b0c-9025-468d-ad6c-d7ea04105edb/",
    "type": "pos",
    "option": "external"
  }
]
```

This endpoint retrieves all payment methods.

### HTTP Request

`GET https://tickets.namespace.ee/api/payment_methods/`

### Query Parameters

Parameter     | Description
------------- | -----------
type          | The type of the payment method
options       | The options of the payment method

## Get a Specific Payment method

> The above command returns JSON structured like this:

```json
{
  "id": "6f527b0c-9025-468d-ad6c-d7ea04105edb",
  "url": "https://tickets.namespace.ee/api/events/6f527b0c-9025-468d-ad6c-d7ea04105edb/",
  "type": "pos",
  "option": "external"
}
```

This endpoint retrieves a specific payment method.

### HTTP Request

`GET https://tickets.namespace.ee/api/payment_methods/<UUID>`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the product group to retrieve
