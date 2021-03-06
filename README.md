# http-echo

A simple node.js HTTP server for testing that will echo back a response, which you can control by passing querystring parameters. 

The server will respond to any URL.

## Available parameters

- `status`: HTTP status code to send back. Defaults to 200.
- `contentType`: MIME type to send back in the Content-Type header. Defaults to 'text/plain'.
- `body`: The body to send back in the response. Defaults to 'hello there!'.

## Example request and response

Request:
```
GET http://localhost:3000/mytest?status=500&contentType=application/json&body={"error":"a message!"}
```

Response:
```HTTP
HTTP/1.1 500 Internal Server Error
Content-Type: application/json
Content-Length: 20
Date: Wed, 10 Apr 2013 21:05:18 GMT
Connection: keep-alive

{"error":"a message!"}
```
