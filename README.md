# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
Name :Selva Kumar A
Reg no: 212222110042
```
### Server code
```
# echo-server.py
import socket

HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
### Client Code:
```
# echo-client.py


import socket
HOST = "127.0.0.1"
PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT)) 
    s.sendall(b"Selva Kumar A,")
    s.sendall(b"212222110042")
    data = s.recv(1024)
print(f"\nRecived {data!r}")
```
## OUTPUT:
### SERVER SIDE
![85810b92-4da8-40d4-b932-bb1785a5b91c](https://github.com/user-attachments/assets/455c4395-72f2-4237-bd1f-85233e525ec9)

### CLIENT SIDE 
![778f154e-3df9-4551-92a6-effb82ced105](https://github.com/user-attachments/assets/eaf9e3b7-0ae8-450d-8169-a70128a80f10)


## RESULT:
The program is executed successfully.
