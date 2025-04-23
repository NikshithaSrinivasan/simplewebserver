# EX01 Developing a Simple Webserver

# Date:23.04.2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```
import http.server
import socketserver

PORT = 8000

class MyHandler(http.server.SimpleHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header("Content-type", "text/html")
        self.end_headers()
        self.wfile.write(b"<html><body><h1>Hi Hello</h1></body></html>")

with socketserver.TCPServer(("", PORT), MyHandler) as httpd:
    print(f"Serving at port {PORT}")
    httpd.serve_forever()
```
# OUTPUT:
![Screenshot 2025-04-23 195009](https://github.com/user-attachments/assets/3ce353e8-2e37-4dc0-8d1e-cf8405bf2b85)



![Screenshot 2025-04-23 105542](https://github.com/user-attachments/assets/0fd40cdc-6f94-4c8c-a516-28c8b971331a)


# RESULT:
The program for implementing simple webserver is executed successfully.
