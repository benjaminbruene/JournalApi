JournalApi

A simple ASP.NET Core Minimal API demonstrating middleware and basic GET endpoints.

Endpoints

GET /

Returns a plain text response.

Example response:

Hello, ASP.NET

GET /time

Returns the current UTC date and time as JSON.

Example response:

{
  "utc": "2026-09-02T23:00:00Z"
}

GET /echo?msg=...

Returns the provided message and the length of the message.

Example request:

/echo?msg=Hello

Example response:

{
  "message": "Hello",
  "length": 5
}

If the msg parameter is missing, the API returns HTTP 400.

Example error response:

{
  "error": "Query parameter 'msg' is required."
}

Middleware

The application adds this response header:

X-App-Name: JournalApi