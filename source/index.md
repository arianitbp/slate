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

This example API documentation page was created with [Slate](http://github.com/tripit/slate).


# Contacts

## Get All Contacts

```shell
curl -X GET -H "Content-type: application/json" -H "Accept: application/json" https://whispering-garden-5307.herokuapp.com/api/db
```

> The above command returns JSON structured like this:

```json
 [
     {
      "id": 1,
      "name": "Hotel1",
      "lastname": "KeyApp1",
      "address": "Prishtine1",
      "phonenumber1": "+38649111111",
      "email": "hotel1@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    },
    {
      "id": 2,
      "name": "Hotel2",
      "lastname": "KeyApp2",
      "address": "Prishtine2",
      "phonenumber1": "+38649111111",
      "email": "hotel2@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    },
    {
      "id": 3,
      "name": "Hotel3",
      "lastname": "KeyApp3",
      "address": "Prishtine3",
      "phonenumber1": "+38649111111",
      "email": "hotel3@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    },
    {
      "id": 4,
      "name": "Hotel4",
      "lastname": "KeyApp4",
      "address": "Prishtine4",
      "phonenumber1": "+38649111111",
      "email": "hotel4@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    },
    {
      "id": 5,
      "name": "Hotel5",
      "lastname": "KeyApp5",
      "address": "Prishtine5",
      "phonenumber1": "+38649111111",
      "email": "hotel5@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    }
 ]
```

This endpoint retrieves all contacts.

### HTTP Request

`GET https://whispering-garden-5307.herokuapp.com/api/db`

### Query Parameters


<aside class="success">
Remember — a happy contact is an authenticated contact!
</aside>

## Get a Specific Contact

```shell
curl -X GET -H "Content-type: application/json" -H "Accept: application/json" https://whispering-garden-5307.herokuapp.com/api/db/<ID>
```

> The above command returns JSON structured like this:

```json
[
    {
      "id": 1,
      "name": "Hotel1",
      "lastname": "KeyApp1",
      "address": "Prishtine1",
      "phonenumber1": "+38649111111",
      "email": "hotel1@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    }
 ]
```

This endpoint retrieves a specific contact.


### HTTP Request

`GET https://whispering-garden-5307.herokuapp.com/api/db/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the contact to retrieve

## Post a Contact

```shell
curl -i -X POST -H "Content-Type: application/json" -d "{""name"":""Hotel1"",""lastname"":""KeyApp1"",""address"":""Prishtine1"",""phonenumber1"":""+38649111111"",""email"":""hotel1@keyapp.com"",""phonenumber2"":""+38649222222"",""phonenumber3"":""+38649333333"",""phonenumber4"":""+38649444444"",""phonenumber5"":""+38649555555""}" https://whispering-garden-5307.herokuapp.com/api/db
```

> The above command returns JSON structured like this:

```json
 [
    {
      "id": 6,
      "name": "Hotel6",
      "lastname": "KeyApp6",
      "address": "Prishtine6",
      "phonenumber1": "+38649111111",
      "email": "hotel6@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    }
 ]
```

This endpoint create a contact.

### HTTP Request

`POST https://whispering-garden-5307.herokuapp.com/api/db`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
ID | auto-increment | ID of a contact generated automatically.
Name | true | If set to false, the result will include contacts that have already been adopted.
LastName | false | If set to true, the result will also include contacts.
Address | false | If set to true, the result will also include contacts.
PhoneNumber1 | false | If set to true, the result will also include contacts.
Email | false | If set to true, the result will also include contacts.
PhoneNumber2 | false | If set to true, the result will also include contacts.
PhoneNumber3 | false | If set to true, the result will also include contacts.
PhoneNumber4 | false | If set to true, the result will also include contacts.
PhoneNumber5 | false | If set to true, the result will also include contacts.

## Put a Contact

```shell
curl -i -X PUT -H "Content-Type: application/json" -d "{""id"":""1"",""name"":""Hotel1"",""lastname"":""KeyApp1"",""address"":""Prishtine1"",""phonenumber1"":""+38649111111"",""email"":""hotel1@keyapp.com"",""phonenumber2"":""+38649222222"",""phonenumber3"":""+38649333333"",""phonenumber4"":""+38649444444"",""phonenumber5"":""+38649555555""}" https://whispering-garden-5307.herokuapp.com/api/db
```

> The above command returns JSON structured like this:

```json
 [
    {
      "id": 1,
      "name": "Hotel1",
      "lastname": "KeyApp1",
      "address": "NewYork",
      "phonenumber1": "+38649111111",
      "email": "hotel1@keyapp.com",
      "phonenumber2": "+38649222222",
      "phonenumber3": "+38649333333",
      "phonenumber4": "+38649444444",
      "phonenumber5": "+38649555555"
    }
 ]
```

This endpoint update a specific contact.


### HTTP Request

`PUT https://whispering-garden-5307.herokuapp.com/api/db`

### URL Parameters

Parameter | Default | Description
--------- | ------- | -----------
ID | true | ID of a contact to update.
Name | false | If set to true, it will change the name of contact.
LastName | false | If set to true, it will change the lastname of contact.
Address | false | If set to true, it will change the address of contact.
PhoneNumber1 | false | If set to true, it will change the phone number of contact.
Email | false | If set to true, it will change the email of contact.
PhoneNumber2 | false | If set to true, it will change the phone number of contact.
PhoneNumber3 | false | If set to true, it will change the phone number of contact.
PhoneNumber4 | false | If set to true, it will change the phone number of contact.
PhoneNumber5 | false | If set to true, it will change the phone number of contact.

## Delete a Contact

```shell
curl -i -X DELETE -H "Content-Type: application/json" -d "{""id"":""2""}" https://whispering-garden-5307.herokuapp.com/api/db
```

> The above command returns JSON structured like this:

```json
 [
    {
      
    }
 ]
```

This endpoint delete a specific contact.


### HTTP Request

`DELETE https://whispering-garden-5307.herokuapp.com/api/db`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the contact to retrieve



