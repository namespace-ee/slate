# Product Groups

## Get All Product Groups

> The above command returns JSON structured like this:

```json
[
  {
    "id": "d55fc97b-65c5-4b34-83ec-18e05242b168",
    "url": "https://tickets.namespace.ee/api/product_groups/d55fc97b-65c5-4b34-83ec-18e05242b168/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "name": "General Access",
    "slug": "general",
    "ordering": 0
  },
  {
    "id": "c70c3823-1c96-410c-96fa-fd7c8271fe13",
    "url": "https://tickets.namespace.ee/api/product_groups/c70c3823-1c96-410c-96fa-fd7c8271fe13/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "name": "Priority",
    "slug": "priority",
    "ordering": 1
  },
  {
    "id": "f39fd97c-4c08-4cb4-aaf7-2342d009cb10",
    "url": "https://tickets.namespace.ee/api/product_groups/f39fd97c-4c08-4cb4-aaf7-2342d009cb10/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "name": "Premium",
    "slug": "premium",
    "ordering": 2
  },
  {
    "id": "62711b76-f5a4-40c5-b356-533783fc6846",
    "url": "https://tickets.namespace.ee/api/product_groups/62711b76-f5a4-40c5-b356-533783fc6846/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "name": "VIP",
    "slug": "vip",
    "ordering": 3
  },
  {
    "id": "b4733342-cf67-406f-8550-f55ba49b7174",
    "url": "https://tickets.namespace.ee/api/product_groups/b4733342-cf67-406f-8550-f55ba49b7174/",
    "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "name": "Camping",
    "slug": "camping",
    "ordering": 4
  }
]
```

This endpoint retrieves all product groups.

### HTTP Request

`GET https://tickets.namespace.ee/api/product_groups/`

### Query Parameters

Parameter     | Description
------------- | -----------
event         | The UUID of the event to filter by

## Get a Specific Product Group

> The above command returns JSON structured like this:

```json
{
  "id": "d55fc97b-65c5-4b34-83ec-18e05242b168",
  "url": "https://tickets.namespace.ee/api/product_groups/d55fc97b-65c5-4b34-83ec-18e05242b168/",
  "event": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "name": "General Access",
  "slug": "general",
  "ordering": 0
}
```

This endpoint retrieves a specific product group.

### HTTP Request

`GET https://tickets.namespace.ee/api/product_groups/<UUID>`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the product group to retrieve
