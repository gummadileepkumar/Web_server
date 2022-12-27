# Developing a Simple Webserver

# AIM:

Name:Gumma Dileep Kumar
ref.no:22007129

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<hl>Welcome</hl>
<h1>dileep kumar</h1>
<h>22007129</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address =('',80)
httpd= HTTPServer(server_address, HelloHandler)
httpd.serve_forever()   


```


# OUTPUT:
![MODEL](/webserver_output.png)

# RESULT:

The program is executed succesfully
