# Errors

<aside class="notice">This error section is stored in a separate file in `includes/_errors.md`. Slate allows you to optionally separate out your docs into many files...just save them to the `includes` folder and add them to the top of your `index.md`'s frontmatter. Files are included in the order listed.</aside>

The REST API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Enter a valid Page
401 | Enter a valid API
404 | Not Found -- The specified contact could not be found
405 | Enter a valid ID
408 | Enter a valid phone-number
412 | Field Name is required
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.
