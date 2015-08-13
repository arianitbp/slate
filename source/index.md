---
title: API Documentation

language_tabs:
  - node.JS

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

The REST API lets you interact with Parse from anything that can send an HTTP request. There are many things you can do with the REST API. For example:

A mobile website can access Parse data from JavaScript.
A webserver can show data from Parse on a website.
You can upload large amounts of data that will later be consumed in a mobile app.
You can download recent data to run your own custom analytics.
Applications written in any programming language can interact with data on Parse.
You can export all of your data if you no longer want to use Parse.

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: ..........`

<aside class="notice">
You must replace `...........` with your personal API key.
</aside>

# Contacts

## Get All Contacts

```node.JS
curl -X GET -H "Content-type: application/json" -H "Accept: application/json" https://whispering-garden-5307.herokuapp.com/api/db
```

> The above command returns JSON structured like this:

```json
 [
    {
      "id": 12,
      "name": "hotelkey",
      "lastname": "app",
      "address": "Prishtine",
      "phonenumber": "1",
      "email": null
    },
    {
      "id": 13,
      "name": "hotelkey1",
      "lastname": "app1",
      "address": "Prishtine1",
      "phonenumber": "12",
      "email": null
    }
 ]
```

This endpoint retrieves all contacts.

### HTTP Request

`GET https://whispering-garden-5307.herokuapp.com/api/db`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Contact

```node.JS
curl -X GET -H "Content-type: application/json" -H "Accept: application/json" https://whispering-garden-5307.herokuapp.com/api/db/<ID>
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Isis",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific contact.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET https://whispering-garden-5307.herokuapp.com/api/db/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the cat to retrieve

