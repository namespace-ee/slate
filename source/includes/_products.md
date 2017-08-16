# Products

## Get All Products

> The above command returns JSON structured like this:

```json
[
  {
    "id": "6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4",
    "url": "https://tickets.namespace.ee/api/products/6a25ee66-d54d-4f89-b2c4-4bcc18fe0cf4/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "group": "https://tickets.namespace.ee/api/product_groups/d55fc97b-65c5-4b34-83ec-18e05242b168/",
    "name": "Primary Ticket",
    "slug": "primary-ticket",
    "description": "Muu lühiinfo.",
    "unit_base": "57.50",
    "unit_vat": "11.50",
    "unit_price": "69.00",
    "vat_percent": "20",
    "state": "active",
    "availability_icon": "green",
    "sales_start": "2017-01-11T08:56:40Z",
    "sales_end": "2017-07-31T20:59:59Z",
    "ordering": 0
  },
  {
    "id": "37109c3a-c262-4fa8-a95a-517b71785aaf",
    "url": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "group": "https://tickets.namespace.ee/api/product_groups/c70c3823-1c96-410c-96fa-fd7c8271fe13/",
    "name": "Second Ticket",
    "slug": "second-ticket",
    "description": "Muu lühiinfo.",
    "unit_base": "65.83",
    "unit_vat": "13.17",
    "unit_price": "79.00",
    "vat_percent": "20",
    "state": "active",
    "availability_icon": "green",
    "sales_start": "2017-01-11T08:56:40Z",
    "sales_end": "2017-07-31T20:59:59Z",
    "ordering": 1
  }
]
```

This endpoint retrieves all products.

### HTTP Request

`GET https://tickets.namespace.ee/api/products/`

### Query Parameters

Parameter     | Description
------------- | -----------
event         | The UUID of the event to filter by
product_group | The UUID of the product group to filter by

## Get a Specific Product

> The above command returns JSON structured like this:

```json
{
  "id": "37109c3a-c262-4fa8-a95a-517b71785aaf",
  "url": "https://tickets.namespace.ee/api/products/37109c3a-c262-4fa8-a95a-517b71785aaf/",
  "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "group": "https://tickets.namespace.ee/api/product_groups/c70c3823-1c96-410c-96fa-fd7c8271fe13/",
  "name": "Second Ticket",
  "slug": "second-ticket",
  "description": "Muu lühiinfo.",
  "unit_base": "65.83",
  "unit_vat": "13.17",
  "unit_price": "79.00",
  "vat_percent": "20",
  "state": "active",
  "availability_icon": "green",
  "sales_start": "2017-01-11T08:56:40Z",
  "sales_end": "2017-07-31T20:59:59Z",
  "ordering": 1
}
```

This endpoint retrieves a specific product.

### HTTP Request

`GET https://tickets.namespace.ee/api/products/<UUID>`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the product to retrieve
