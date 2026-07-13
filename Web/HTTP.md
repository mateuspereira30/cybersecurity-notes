# HTTP and HTTPS
## General Concept

Hypertext Transfer Protocol (HTTP) is used for communication between distributed and collaborative hypermedia information systems. HTTP is the foundation of communication on the World Wide Web (WWW).

Hypertext is structured text that uses logical links to connect text, images, audio, videos, advertisements, and other web pages.

Communication follows a client-server model. Requests are sent by an entity called the user agent (or a proxy acting on its behalf). Most of the time, the user agent is a web browser, but it can also be another program, such as a web crawler or a bot.

HTTP is designed to be simple and easy to read and understand.

It is also extensible. Headers make it easy to extend HTTP and experiment with new features. New functionality can be added after an agreement between the client and the server.

HTTP is stateless, meaning there is no relationship between two separate requests. This is why cookies exist: they are used to store session information.

Authentication allows some pages to be protected so that only specific users can access them.

HTTPS is HTTP over SSL/TLS.

## Structure of an HTTP Request

Every HTTP request is composed of different parts, each with a specific role in the communication between the client and the server.

The first line of the request, known as the Request Line, contains three key pieces of information:

### HTTP Method: Defines the action that the client wants to perform on a resource, such as retrieving, creating, updating, or deleting data.

### Request Path: Identifies the resource that the client wants to access on the server.
HTTP Version: Indicates which version of the HTTP protocol is used to process the request.

After the Request Line, the headers are sent. They carry additional information about the request, such as the content type, authentication data, cookies, the user agent, and other settings required for communication.

Some requests may also include a message body, which is used to send data to the server. This is common in methods such as POST, PUT, and PATCH, but it is usually absent in GET requests.

## HTTP Methods

HTTP methods define the action that the client wants to perform on a specific resource. Each method has a specific purpose and should be used according to the intended operation.

### GET

Used to retrieve a resource from the server. Its purpose is to obtain information without modifying the resource's state.

### POST

Used to send data to the server, usually to create a new resource or submit information for processing.

### PUT

Used to create a new resource or completely replace an existing one. If the resource already exists, its content is completely overwritten.

### PATCH

Used to partially update an existing resource by modifying only the specified fields instead of replacing the entire resource.

### DELETE

Used to remove a specific resource from the server.

### HEAD

Works similarly to the GET method but returns only the response headers, without the response body. It is used to verify whether a resource exists or to retrieve information about it without transferring its content.

### OPTIONS

Returns the HTTP methods and communication options supported by a resource. It is commonly used by web browsers during CORS preflight requests.

## HTTP Responses

After receiving and processing a request, the server sends an HTTP response to the client. This response informs the client whether the request was successful, whether an error occurred, or whether additional action is required, such as following a redirect.

An HTTP response consists of three main parts:

### Status Line: Contains the HTTP protocol version, the status code, and a brief description of the request's outcome.

### Headers: Store additional information about the response, such as the content type, content length, cookies, and cache instructions.

### Message Body: Contains the data returned by the server, such as an HTML page, a JSON document, an image, or any other type of content. In some responses, the message body may be absent.

## Most Common HTTP Status Codes
### 2xx - Success
200 OK – The request was successful.
201 Created – The request was successful, and a new resource was created.
204 No Content – The request was successful, but there is no content to return.
### 3xx - Redirection
301 Moved Permanently – The requested resource has been permanently moved to a new URL.
302 Found – Temporarily redirects the client to another URL.
304 Not Modified – Indicates that the cached version of the resource is still valid.
307 Temporary Redirect – Temporarily redirects the client while preserving the original HTTP method.
308 Permanent Redirect – Permanently redirects the client while preserving the original HTTP method.
### 4xx - Client Errors
400 Bad Request – The server could not understand the request due to invalid syntax.
401 Unauthorized – Authentication is required to access the resource.
403 Forbidden – The server understands the request but refuses to authorize it.
404 Not Found – The requested resource could not be found.
405 Method Not Allowed – The request method is not allowed for the target resource.
429 Too Many Requests – The client has sent too many requests in a given amount of time, usually due to rate limiting.
### 5xx - Server Errors
500 Internal Server Error – An unexpected error occurred on the server.
502 Bad Gateway – The server received an invalid response from an upstream server.
503 Service Unavailable – The server is temporarily unavailable.


##HTTP is the foundation of Web Security.

Understanding HTTP requests and responses is essential for identifying vulnerabilities such as:

- SQL Injection
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Server-Side Request Forgery (SSRF)
- HTTP Request Smuggling
- Authentication flaws
