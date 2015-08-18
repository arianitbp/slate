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

This example API documentation page was created with [Slate](http://github.com/arianitbp/slate).


# Contacts

## Get All Contacts

```shell
curl -X GET -H "Content-type: application/json" -H "Accept: application/json" "https://whispering-garden-5307.herokuapp.com/api/db"
```

> The above command returns JSON structured like this:

```json
{   "success": "Database Read with success.",
	 "data":[
				 {
				  "id": 1,
				  "name": "Hotel1",
				  "lastname": "KeyApp1",
				  "address": "Prishtine1",
				  "email": "hotel1@keyapp.com",
				  "phonenumber1": "+38649111111",
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
				  "email": "hotel2@keyapp.com",
				  "phonenumber1": "+38649111111",
				  "phonenumber4": "+38649444444",
				  "phonenumber5": "null"
				},
				{
				  "id": 3,
				  "name": "Hotel3",
				  "lastname": "KeyApp3",
				  "address": "Prishtine3",
				  "email": "hotel3@keyapp.com",
				  "phonenumber2": "0038649222222",
				  "phonenumber3": "0038649333333",
				  "phonenumber4": "0038649444444"
				}
			]
}
```

- This endpoint retrieves all contacts.

### HTTP Request

`GET https://whispering-garden-5307.herokuapp.com/api/db`

### Query Parameters


<aside class="success">
Remember — a happy contact is an authenticated contact!
</aside>

## Get a Specific Contact

```shell
curl -X GET -H "Content-type: application/json" -H "Accept: application/json" "https://whispering-garden-5307.herokuapp.com/api/db/<ID>"
```

> The above command returns JSON structured like this:

```json
{   "success": "Database Read with success.",
	 "data":[
				 {
				  "id": 1,
				  "name": "Hotel1",
				  "lastname": "KeyApp1",
				  "address": "Prishtine1",
				  "email": "hotel1@keyapp.com",
				  "phonenumber1": "+38649111111",
				  "phonenumber2": "+38649222222",
				  "phonenumber3": "+38649333333",
				  "phonenumber4": "+38649444444",
				  "phonenumber5": "+38649555555"
				},  
			]
}
```

- This endpoint retrieves a specific contact.


### HTTP Request

`GET https://whispering-garden-5307.herokuapp.com/api/db/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the contact to retrieve

<aside class="warning">This will returns an error if you don't use any ID.</aside>

## Post a Contact

```shell
curl -i -X POST -H "Content-Type: application/json" -d "{""name"":""Hotel1"",""lastname"":""KeyApp1"",""address"":""Prishtine1"",""phonenumber1"":""+38649111111"",""email"":""hotel1@keyapp.com"",""phonenumber2"":""+38649222222"",""phonenumber3"":""+38649333333"",""phonenumber4"":""+38649444444"",""phonenumber5"":""+38649555555""}" 
"https://whispering-garden-5307.herokuapp.com/api/db"
```

> The above command returns JSON structured like this:

```json
{
	"success": "Contact inserted with success into database."
}
```

- This endpoint create a contact.

### HTTP Request

`POST https://whispering-garden-5307.herokuapp.com/api/db`

### Query Parameters

Parameter | Default | Type | Description
--------- | ------- | ------- | -----------
ID | auto-increment, false | integer | ID of a contact generated automatically.
Name | true | text | If set to false, the result will include contacts that have already been adopted.
LastName | false | text | If set to true, the result will also include contacts.
Address | false | text | If set to true, the result will also include contacts.
PhoneNumber1 | false | text | If set to true, the result will also include contacts.
Email | false | text | If set to true, the result will also include contacts.
PhoneNumber2 | false | text | If set to true, the result will also include contacts.
PhoneNumber3 | false | text | If set to true, the result will also include contacts.
PhoneNumber4 | false | text | If set to true, the result will also include contacts.
PhoneNumber5 | false | text | If set to true, the result will also include contacts.

<aside class="notice">If you forget to fill the field of Name then can't create any contact. For other fields doesn't matter.</aside>

## Put a Contact

```shell
curl -i -X PUT -H "Content-Type: application/json" -d "{""id"":""1"",""name"":""Hotel1"",""lastname"":""KeyApp1"",""address"":""Prishtine1"",""phonenumber1"":""+38649111111"",""email"":""hotel1@keyapp.com"",""phonenumber2"":""+38649222222"",""phonenumber3"":""+38649333333"",""phonenumber4"":""+38649444444"",""phonenumber5"":""+38649555555""}" 
"https://whispering-garden-5307.herokuapp.com/api/db"
```

> The above command returns JSON structured like this:

```json
{
	"success": "Contact updated with success into database."
}
```

- This endpoint update a specific contact.


### HTTP Request

`PUT https://whispering-garden-5307.herokuapp.com/api/db`

### URL Parameters

Parameter | Default | Type | Description
--------- | ------- | ------- | -----------
ID | true | integer | ID of a contact to update.
Name | false | text | If set to true, it will change the name of contact.
LastName | false | text | If set to true, it will change the lastname of contact.
Address | false | text | If set to true, it will change the address of contact.
PhoneNumber1 | false | text | If set to true, it will change the phone number of contact.
Email | false | text | If set to true, it will change the email of contact.
PhoneNumber2 | false | text | If set to true, it will change the phone number of contact.
PhoneNumber3 | false | text | If set to true, it will change the phone number of contact.
PhoneNumber4 | false | text | If set to true, it will change the phone number of contact.
PhoneNumber5 | false | text | If set to true, it will change the phone number of contact.

<aside class="notice">It will return error if you don't use an ID.</aside>

## Delete a Contact

```shell
curl -i -X DELETE -H "Content-Type: application/json" -d "{""id"":""2""}" "https://whispering-garden-5307.herokuapp.com/api/db"
```

> The above command returns JSON structured like this:

```json
 [
    {
      "success": "Contact updated with success in the database."
    }
 ]
```

- This endpoint delete a specific contact.


### HTTP Request

`DELETE https://whispering-garden-5307.herokuapp.com/api/db`

### URL Parameters

Parameter | Requirement | Type | Description
--------- | ----------- | --------- | -----------
ID | true | integer | The ID of the contact to retrieve

<aside class="notice">When you want to delete a contact you can do it by chosing any ID.</aside>