# EX01 Developing a Simple Webserver

# Date:19-09-2025
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
from http.server import BaseHTTPRequestHandler,HTTPServer
content ='''
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
   
</head>

<body bgcolor="black" text="white">
<style>
.a
{
height:500px;
margin-top:200px;
width:600px;
padding:4px;

background-image:linear-gradient(to right top, #d16ba5, #c777b9, #ba83ca, #aa8fd8, #9a9ae1, #8aa7ec, #79b3f4, #69bff8, #52cffe, #41dfff, #46eefa, #5ffbf1);

}
</style>
<body background-color="white">
<center>
<div class="a">
<h1>My Laptop Specification</h1>

<h4>Device name:LAPTOP-K69113SN</h4>
<h4>Processor:13th Gen Intel(R) Core(TM) i7-13620H (2.40 GHz)</h4>
<h4>Installed RAM:16.0 GB (15.6 GB usable)</h4>
<h4>Device ID:747BDE2B-599D-439B-96DB-8308C71B5BD9</h4>
<h4>Product ID	:00342-42754-71123-AAOEM</h4>
<h4>System type	64-bit operating system, x64-based processor</h4>
<h4>Pen and touch:No pen or touch input is available for this display</h4>
<h4>Graphics: Integrated Intel® Arc™ Graphics. </h4>
<h4>Memory: Up to 16GB LPDDR5X RAM. </h4>
<h4>Storage: Up to 1TB M.2 NVMe™ PCIe® 4.0 SSD. </h4>
</pre>
</div>
</center>
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
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,Myserver)
httpd.serve_forever()
```
# OUTPUT:
![alt text](<Screenshot 2025-09-19 115808.png>)
![alt text](<Screenshot 2025-09-19 115825.png>)

# RESULT:
The program for implementing simple webserver is executed successfully.
