HTTP and HTTPS
General Concept

Hypertext Transfer Protocol (HTTP) is used for communication between distributed and collaborative hypermedia information systems. HTTP is the foundation of communication on the World Wide Web (WWW).

Hypertext is structured text that uses logical links to connect text, images, audio, videos, advertisements, and other web pages.

Communication follows a client-server model. Requests are sent by an entity called the user agent (or a proxy acting on its behalf). Most of the time, the user agent is a web browser, but it can also be another program, such as a web crawler or a bot.

HTTP is designed to be simple and easy to read and understand.

It is also extensible. Headers make it easy to extend HTTP and experiment with new features. New functionality can be be added after an agreement between the client and the server.

HTTP is stateless, meaning there is no relationship between two separate requests. This is why cookies exist: they are used to store session information.

Authentication allows some pages to be protected so that only specific users can access them.

HTTPS is HTTP over SSL/TLS.

Structure of an HTTP Request

Every HTTP request is composed of different parts, each with a specific role in the communication between the client and the server.

The first line of the request, known as the Request Line, contains three key pieces of information:

HTTP Method: Defines the action that the client wants to perform on a resource, such as retrieving, creating, updating, or deleting data.
Request Path: Identifies the resource that the client wants to access on the server.
HTTP Version: Indicates which version of the HTTP protocol is used to process the request.

After the Request Line, the headers are sent. They carry additional information about the request, such as the content type, authentication data, cookies, the user agent, and other settings required for communication.

Some requests may also include a message body, which is used to send data to the server. This is common in methods such as POST, PUT, and PATCH, but it is usually absent in GET requests.

HTTP Methods

HTTP methods define the action that the client wants to perform on a specific resource. Each method has a specific purpose and should be used according to the intended operation.

GET

Used to retrieve a resource from the server. Its purpose is to obtain information without modifying the resource's state.

POST

Used to send data to the server, usually to create a new resource or submit information for processing.

PUT

Used to create a new resource or completely replace an existing one. If the resource already exists, its content is completely overwritten.

PATCH

Used to partially update an existing resource by modifying only the specified fields instead of replacing the entire resource.

DELETE

Used to remove a specific resource from the server.

HEAD

Works similarly to the GET method but returns only the response headers, without the response body. It is used to verify whether a resource exists or to retrieve information about it without transferring its content.

OPTIONS

Returns the HTTP methods and communication options supported by a resource. It is commonly used by web browsers during CORS preflight requests.
