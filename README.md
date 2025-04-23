# EX01 Developing a Simple Webserver

# Date:19/04/2025
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
```python
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<html>
<head>
    <title>TCP/IP Protocol Suite</title>
</head>
<body>
    <h1>TCP/IP Protocol Suite</h1>
    <ul>
        <li><strong>Application Layer</strong>
            <ul>
                <li>HTTP, HTTPS</li>
                <li>FTP, TFTP</li>
                <li>SMTP, POP3, IMAP</li>
                <li>DNS</li>
                <li>Telnet, SSH</li>
            </ul>
        </li>
        <li><strong>Transport Layer</strong>
            <ul>
                <li>TCP</li>
                <li>UDP</li>
            </ul>
        </li>
        <li><strong>Internet Layer</strong>
            <ul>
                <li>IP (IPv4, IPv6)</li>
                <li>ICMP, IGMP</li>
                <li>ARP</li>
            </ul>
        </li>
        <li><strong>Network Access Layer</strong>
            <ul>
                <li>Ethernet</li>
                <li>Wi-Fi</li>
                <li>PPP</li>
            </ul>
        </li>
    </ul>
</body>
</html>

'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()


```
# OUTPUT:

![Screenshot 2025-04-23 155922](https://github.com/user-attachments/assets/f6d4dcfb-afac-4739-9682-e3ca86bbf553)

![Screenshot 2025-04-23 105542](https://github.com/user-attachments/assets/0fd40cdc-6f94-4c8c-a516-28c8b971331a)


# RESULT:
The program for implementing simple webserver is executed successfully.
