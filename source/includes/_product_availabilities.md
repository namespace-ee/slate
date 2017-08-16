# Product Availabilities

## Get All Product Availabilities

> The above command returns JSON structured like this:

```json
[
  {
    "product": "https://tickets.namespace.ee/api/products/6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4/",
    "quantity": 6
  },
  {
    "product": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf/",
    "quantity": 4
  }
]
```

This endpoint retrieves all product availabilities.

### HTTP Request

`GET https://tickets.namespace.ee/api/product_availabilities/`

### Query Parameters

Parameter     | Description
------------- | -----------
event         | The UUID of the event to filter by
product       | The UUID of the product to filter by
product_group | The UUID of the product_group to filter by
