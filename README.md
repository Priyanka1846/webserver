# Developing a Simple Webserver

NAME : PRIYANKA K
REGISTER NO. : 212223230162

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```

content="""
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1> Top five Web Application Development Frameworks </h1>
<h2> 1.Django </h2>
<h2> 2. MEAN Stack </h2>
<h2> 3. REACT </h2>
<h2> 4.  RUBY ON RAILS</h2>
<h2> 5. ASP.NET </h2>

</body>
</html>



"""
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved...")
        self.send_response(200)
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my Webserver")
server_address=('', 80)
httpd=HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
## OUTPUT:
![image](https://github.com/Priyanka1846/webserver/assets/139425809/e15cb79c-0991-4218-9ec7-12a4e0253779)
![image](https://github.com/Priyanka1846/webserver/assets/139425809/f77f3607-b2b8-4b18-84cd-051ef995efcb)


## RESULT:
The program is executed succesfully
