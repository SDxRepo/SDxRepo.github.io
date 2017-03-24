---
weight: 90
title: Errors

---

# Errors

<aside class="notice">Common API Errors should generally align with the industry standard</aside>

The SportDx API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request sucks
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- For administrators only
404 | Not Found -- The specified endpoint could not be found
405 | Method Not Allowed -- You tried to access an endpoint with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
410 | Gone -- The endpoint requested has been removed from our servers
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarially offline for maintanance. Please try again later.