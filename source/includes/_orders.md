# Orders

## List Orders

> The above command returns JSON structured like this:

```json
[
  {
    "id": "166a1ddb-492c-49a0-a84c-2465b9b43f01",
    "url": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
    "name": "Awesome Festival 2017",
    "slug": "awesome-festival-2017",
    "date_start": "2017-09-03",
    "date_end": "2017-09-05",
    "venue": "Linnahall",
    "website": "http://awesome-festival.ee/",
    "support_email": "info@awesome-festival.ee"
  }
]
```

This endpoint retrieves all the events.

### HTTP Request

`GET https://tickets.namespace.ee/api/events/`

## Get a Specific Event

> The above command returns JSON structured like this:

```json
{
  "id": "166a1ddb-492c-49a0-a84c-2465b9b43f01",
  "url": "https://tickets.namespace.ee/api/events/166a1ddb-492c-49a0-a84c-2465b9b43f01/",
  "name": "Awesome Festival 2017",
  "slug": "awesome-festival-2017",
  "date_start": "2017-09-03",
  "date_end": "2017-09-05",
  "venue": "Linnahall",
  "website": "http://awesome-festival.ee/",
  "support_email": "info@awesome-festival.ee"
}
```

This endpoint retrieves a specific event.

### HTTP Request

`GET https://tickets.namespace.ee/api/events/<UUID>`

### URL Parameters

Parameter | Description
--------- | -----------
UUID      | The UUID of the event to retrieve
