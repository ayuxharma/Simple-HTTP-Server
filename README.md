# Simple-HTTP-Server
The server listens for incoming connections on a port 8080. and processes client requests in separate threads. This allows the server to handle multiple concurrent connections.

Upon receiving a client request, the server checks if it is a valid GET request and extracts the requested file name. It then decodes the URL-encoded file name and determines the file's extension to identify the appropriate MIME type for the response.

Using a case-insensitive file search, the server checks if the requested file exists in the current directory. If it does, the server constructs an HTTP response with the appropriate headers, including the determined MIME type, and sends the file's contents to the client. If the file is not found, the server sends a 404 Not Found response.

The server continues to accept and process incoming connections until it is manually terminated.
