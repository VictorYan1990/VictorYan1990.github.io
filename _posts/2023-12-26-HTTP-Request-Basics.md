---
layout: post
title:  "Beginners' Guide of HTTP Request"
date:   2023-12-26 3:26:26 -0500
categories: "Web Development"
tags: "Web Development"
---

### Request Overview

A complete HTTP request generally include two parts: request headers and request body. Examples as follows:

GET request
```http 
GET https://example.com/api/resource?param1=value1&param2=value2 HTTP/1.1
Host: example.com
```
POST request
```http
POST https://example.com/submit-form HTTP/1.1
Host: example.com
Content-Type: application/x-www-form-urlencoded
Cookie: session_id=12345
param1=value1&param2=value2
```
When we say request header, its' actually not just one header, instead a bunch. In the examples above, HOST, Method, Cookie, and Content-Type are all headers.

Typically, GET request has no request body. When we say request, it usually comes when we submit a request through certain web forms. For GET request, all required information are embeddied within url.
When you type an url to the address box of a browser, in default a GET request is made. That is why we never see a method (GET,POST,...) symbol is passed along with the url, nor we need to specify request method.

HTTP is TCP request. Thus it has to be delivered to a port of certain IP. A domain is substantially a registered combination of IP:port.

### Understand URL
Any typical URL can be break down to following four parts:
>http_header://domain/request/parameters

or 

>http_header://IP:port/request{identifier}{parameters}

Here {identifier} can be ?/#, and then parameters will follow key=var format seperated by &/; correspondently. 

The responsibility for parsing and interpreting the special characters in a URL, such as "?" and "#", falls primarily on the HTTP server and the web browser (client-side).

The browser identifies the parts of the URL, including the scheme (e.g., "http" or "https"), host (e.g., "example.com"), path (e.g., "/resource"), query parameters (e.g., "?param1=value1&param2=value2"), and fragment identifier (e.g., "#section"). Then the browser uses this information to make an **HTTP request** to the appropriate server and to render the web page accordingly.

The **HTTP server**, on the receiving end of the request, is responsible for processing the URL and route the request to the appropriate handler or resource based on the path and query parameters.
The server typically uses the path to determine the route, and it can access the query parameters to extract additional information needed to generate a response.

On the other hand when path parameters are used in a URL, both the browser and the HTTP server treat the entire URL as part of the path, without parsing it into separate parameters. The web server then delivers the entire URL to the web application server, where views or handlers can parse the path and extract the necessary information from it.