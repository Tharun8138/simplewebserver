# ﻿EX01 Developing a Simple Webserver
## Date:05.12.2024
## AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

## DESIGN STEPS:
### Step 1:
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver


## CODE:
```
<!DOCTYPE html>
<head>
    <title>LAPTOP CONFIGURATION</title>
</head>

<body><center>
    <h1>My laptop configuration</h1>THARUN.V<h1></h1></center>
    <table border="100px" align="center" cellpadding="10" style="background-color: rgb(76, 76, 205);" >
    <tr style="color: black; ">
        <th>DEVICE SPECIFICATION</th>
        <th>DETAILS</th>
    </tr>
    <tr style="color: rgb(0, 0, 0); ">
        <td>BRAND</td>
        <td>LENOVO</td>
    </tr>
    <tr>
        <td>MODEL NAME</td>
        <td>E16 GEN 4</td>
    </tr>
    <tr>
        <td>SCREEN SIZE</td>
        <td>15.6 inches</td>
    </tr>
    <tr>
        <td>COLOR</td>
        <td>BLACK</td>
    </tr>
    <tr>
        <td>RAM</td>
        <td>16GB</td>
    </tr>
    <tr>
        <td>ROM</td>
        <td>512GB</td>
    </tr>    
    <tr>
        <td>HARD DISK</td>
        <td>CORE i5</td>
    </tr>
    <tr>
        <td>GRAPHICS CARD</td>
        <td>NVIDIA</td>
    </tr>
    <tr>
        <td>SYSTEM TYPE</td>
        <td>64 BIT-OS,X64</td>
    </tr>
</table>

</body>
```
## simplewebserver1.html
```
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```




## OUTPUT:
![Screenshot 2024-11-25 103916](https://github.com/user-attachments/assets/fb6ebaff-534a-4412-a4f5-1858828b5a91)
![Screenshot 2024-12-05 140556](https://github.com/user-attachments/assets/412aa4a2-2382-434f-ad02-abe7b773316f)



## RESULT:
The program for implementing simple webserver is executed successfully.
