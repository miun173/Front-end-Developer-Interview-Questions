---
title: Network Questions
layout: layouts/page.njk
permalink: /questions/network-questions/index.html
---

* Traditionally, why has it been better to serve site assets from multiple domains?
  - If its a CDN as, it's good. With CDN it will fetch the assets from the closest place 
  
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
  - When we type a URL, the browser will look through DNS if the URL exists, 
  - if it there, the browser will handshake with our server
  - The htm are being downloaded.
  - The browser begin to parse
  - when it sees external resource lik css, or js, it will downloaded them too
  - the browser will parse everything including js before it displayed
  - after all parse are done it will render the result to users
  
* What are the differences between Long-Polling, Websockets and Server-Sent Events?
  - WebSocket `Full-duplex`
    Websocket is a full-duplex communication channels over a single TCP connection. When both server and browser support, it is the only transport that establishes a true persistent, two-way connection between client and server.

  - Server Sent Events `Simplex`
  also known as EventSource is a technology where a browser receives automatic updates from a server via HTTP connection. The Server-Sent Events EventSource API is standardized as part of HTML5 by the W3C.

  - Ajax long polling `(One Request -> One Response [but delayed]) repeated`
  Long polling does not create a persistent connection, but instead polls the server with a request that stays open until the server responds, at which point the connection closes, and a new connection is requested immediately. This may introduce some latency while the connection resets

* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
  
  - Expires headers tell the browser whether they should request a specific file from the server or whether they should grab it from the browser's cache.
  - Date: The date and time that the message was sent
  - The Age response-header field conveys the sender's estimate of the amount of time since the response (or its revalidation) was generated at the origin server.
  - The If-Modified-Since request-header field is used with a method to make it conditional: if the requested variant has not been modified since the time specified in this field, an entity will not be returned from the server; instead, a 304 (not modified) response will be returned without any message-body.
  - Do Not Track: disable either its tracking or cross-site user tracking 
  - Cache-Control: Tells all caching mechanisms from server to client whether they may cache this object. It is measured in seconds
  - Transfer-Encoding: The form of encoding used to safely transfer the entity to the user. Currently defined methods are: chunked, compress, deflate, gzip, identity.
  - ETag: An identifier for a specific version of a resource.
  - X-Frame-Options can be used to indicate whether or not a browser should be allowed to render a page in a <frame>, <iframe> or <object> .
  
* What are HTTP methods? List all HTTP methods that you know, and explain them.
  - GET: The GET method is used to retrieve information from the given server using a given URI. Requests using GET should only retrieve data and should have no other effect on the data.
  - HEAD: Same as GET, but transfers the status line and header section only.
  - POST: A POST request is used to send data to the server, for example, customer information, file upload, etc. using HTML forms.
  - PUT: Replaces all current representations of the target resource with the uploaded content.
  - DELETE: Removes all current representations of the target resource given by a URI.
  - CONNECT: Establishes a tunnel to the server identified by a given URI.
  - OPTIONS: Describes the communication options for the target resource.
  - TRACE: Performs a message loop-back test along the path to the target resource.
