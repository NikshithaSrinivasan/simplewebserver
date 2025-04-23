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
from http.server import HTTPServer,BaseHTTPRequestHandler

```
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

```
```
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

```


```
# OUTPUT:
![nikshi](https://github.com/user-attachments/assets/0725f7ff-a0d6-45e2-a416-cbfa2064fc20)


![nikshi](https://github.com/user-attachments/assets/4f2c397c-bc11-4727-af47-9e9fc0bf7b50)



# RESULT:
The program for implementing simple webserver is executed successfully.
