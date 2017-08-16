---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - http

# toc_footers:
#   - <a href='#'>Sign Up for a Developer Key</a>
#   - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - events
  - products
  - product_groups
  - product_availabilities
  - payment_methods

search: true
---

# Introduction

Tickets API is a RESTful web service for developers to programmatically interact with Events, Products, Tickets sales data etc.

The Tickets API is organized around REST. Every bit of data exchanged between clients and the API is JSON over HTTPS. All API requests must be made over HTTPS. Calls made over plain HTTP will fail. You must authenticate for all requests.

The base URL for the Tickets API is [https://tickets.namespace.ee/api/](https://tickets.namespace.ee/api/).

* The API is a RESTful webservice running over HTTPS connections
* Each client authenticates with the service using a token in the Authorization header
* All request and response contents are encoded in JSON
* Clients must send "application/json" in the Accept and Content-Type headers
* All datetime values are encoded in timezone-aware ISO8601
* The service uses HTTP response codes to communicate the successes and failures
* Any incoming request is subject to validation and in case of errors a HTTP 400 Bad Request
  will be sent together with detailed failure message in the response body.
* List requests are subject to pagination. A hyperlink to the next page is provided
  in the Link header together with the rel="next" attribute.
* A client must respect the HTTP 429 Too Many Requests status code in overload conditions.

If you have questions about using the API, or have come across a bug you’d like to report, write us an email at [tickets@namespace.ee](tickets@namespace.ee).

## Authentication

For clients to authenticate, the token key should be included in the Authorization HTTP header.

The key should be prefixed by the string literal "Token", with whitespace separating the two strings.

`Authorization: Token 9944b09199c62bcf9418ad846dd0e4bbdfc6ee4b`

<aside class="notice">
You must replace <code>9944b09199c62bcf9418ad846dd0e4bbdfc6ee4b</code> with your personal API key.
</aside>

Unauthenticated responses that are denied permission will result in an HTTP 401 Unauthorized response with an appropriate WWW-Authenticate header.

`WWW-Authenticate: Token`

## Obtaining authentication tokens

To obtain a authentication token the fallowing HTTP request has to be performed.

> The request returns JSON structured like this:

```json
{
  "token": "7e9917ffg57b043b9527711395c013761b2113c7"
}
```

### HTTP Request

`POST https://gsmtasks.com/api/authenticate/`

### Query Parameters

Parameter | Type   | Required | Description
--------- | ------ | -------  | -----------
username  | String | yes      | The email used during signup
password  | String | yes      | The password set for that username

<aside class="success">
The tokens are valid forever, unless refreshed by the user himself.
</aside>

## Response Status codes and errors

Tickets API uses conventional HTTP response codes to indicate success or failure of an API request. In general, codes in the 2xx range indicate success, codes in the 4xx range indicate an error that resulted from the provided information (e.g. a required parameter was missing, a charge failed, etc.), and codes in the 5xx range indicate an error with Tickets API servers.

Status code | Status text       | Description
----------- | ----------------- | -----------
200         | OK                | Everything worked as expected.
400         | Bad Request       | Often missing a required parameter.
401         | Unauthorized      | No valid API key provided.
402         | Request Failed    | Parameters were valid but request failed.
404         | Not Found         | The requested item doesn't exist.
429         | Too Many Requests | Too many requests hit the API too quickly.
50*         | Server Errors     | Something went wrong on our end.
