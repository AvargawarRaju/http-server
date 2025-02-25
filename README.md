# http-server
import { createServer } from 'node:http'; 

The createServer function is imported from the built-in node:http module. 

This function is used to create an HTTP server. 

The createServer function takes a callback function as an argument. 

This callback is executed every time the server receives an HTTP request. 

The callback receives two objects: 

📌 req: The request object, which contains information about the incoming HTTP request (e.g., URL, headers, etc.). 

📌 res: The response object, which is used to send data back to the client. 

const server = createServer((req, res) => { 

 res.writeHead(200, { 'Content-Type': 'text/plain' }); 

 res.writeHead sets the HTTP status code and response headers. 

✅ 200: The HTTP status code for "OK" (successful response). 

✅ { 'Content-Type': 'text/plain' }: Specifies that the response body will be plain text. 

 res.end('Hello World!\n'); 

}); 

res.end sends the response body and ends the response process. 

In this case, the response body is the string 'Hello World!\n'. 

// 🌟 Starts a simple HTTP server locally on port 3000 

server.listen(3000, '127.0.0.1', () => { 

 console.log('Listening on 127.0.0.1:3000'); 

}); 

The server.listen method starts the server and makes it listen for incoming requests. 

It takes three arguments: 

🔹 3000: The port number on which the server will listen. 

🔹 '127.0.0.1': The IP address of the server (in this case, localhost). 

🔹 A callback function that logs a message once the server starts listening. 

✨ Run the server: 

💻 node server.mjs 

Once running, you can access the server by navigating to: 

🌍 http://127.0.0.1:3000 in your browser or using a tool like curl. 
