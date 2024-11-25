EX01 Developing a Simple Webserver
Date:
AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

DESIGN STEPS:
Step 1:
HTML content creation.

Step 2:
Design of webserver workflow.

Step 3:
Implementation using Python code.

Step 4:
Serving the HTML pages.

Step 5:
Testing the webserver.

PROGRAM:

simplewebserver1.html




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

simplewebserver1.html
OUTPUT:
![Screenshot 2024-11-25 103916](https://github.com/user-attachments/assets/fb6ebaff-534a-4412-a4f5-1858828b5a91)



RESULT:
The program for implementing simple webserver is executed successfully.
