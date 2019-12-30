# Errors

<aside class="notice">
Listed below are the errors that are common across all APIs. Where invididual APIs can return different errors they will
be listed out separately in those sections.
</aside>

> All errors will have the following JSON attached containing more detail about the error message.

```json
{
  "error": "More detail about the error",
  "status": 400
}
```

The TruCentive API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid, please see the json error.
403 | Access Denied -- Your API key is wrong or your OAuth account is not authorized.
404 | Not Found -- The specified API or resource could not be found.
406 | Not Acceptable -- You requested a format that isn't valid.
429 | Too Many Requests -- You've submitted too many API requests in too short a time, try again later.
500 | Internal Server Error -- We had a problem processing your request, please try again later or contact support.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
