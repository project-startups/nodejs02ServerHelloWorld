# Node.js Simplest Web Server

## To run the application:

1. Clone the repository **_OR_**
   Create a new file called `server.js` and copy all contents from `server.js` file of this repository to locally created `server.js` file.
2. To run this snippet run `node server.js` or `node server` in your terminal.

3. Open your web browser and run the following address: `http://127.0.0.1:3000/`

## Explaination

- This code first includes the Node.js `http module`.
- The `createServer()` method of `http` creates a new **HTTP server** and returns it.
- The server is set to listen on the specified port and host name. When the server is ready, the **callback** function is called, in this case informing us that the server is running.

- Whenever a new request is received, the **`request event`** is called, providing two objects: a request (an **`http.IncomingMessage object`**) and a response (an **`http.ServerResponse`** object).

- Those 2 objects are essential to handle the HTTP call.

- The first provides the request details. In this simple example, this is not used, but you could access the **`request headers`** and **`request data`**.

- The second is used to return data to the caller.

  In this case with:

  ```js
  res.statusCode = 200;
  ```

  we set the statusCode property to 200, to indicate a successful response.

  We set the Content-Type header:

  ```js
  res.setHeader("Content-Type", "text/plain");
  ```

  and we close the response, adding the content as an argument to end():

  ```js
  res.end("Hello World\n");
  ```
