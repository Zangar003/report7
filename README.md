# report7
This is a Go program for a web application that allows users to upload and view files.

The program defines a few functions:

dbConn(): Connects to a MySQL database and returns a handle to the connection.
upload(): Queries the database to retrieve information about uploaded files, and then renders an HTML template to display the information on a web page.
uploadFiles(): Handles HTTP POST requests that contain uploaded files, and saves the files to a temporary directory on the server. It also inserts information about the files into the database.
delete(): Deletes a file from the database based on its ID.
handleRequest(): Registers HTTP handlers for various routes and starts the HTTP server.
The program also defines a upfile struct, which represents a file that has been uploaded.

In the main() function, handleRequest() is called to start the HTTP server. The server listens on port 9000 and serves static files from the "static" directory.

Note that the program uses template.Must to load HTML templates from the "static/templates" directory, and it assumes that the templates have a ".html" file extension. It also uses log.Println() to log messages to the console.
