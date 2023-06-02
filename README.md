# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

# DATE : 25-04-2023
# AIM :

To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.
# ALGORITHM :

    Import the necessary modules in python
    Create a socket connection to using the socket module.
    Send message to the client and receive the message from the client using the Socket module in server.
    Send and receive the message using the send function in socket.

# PROGRAM :
# Client:

# Developed by: Lavanya S
# Register No: 212221220030
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
msg=input("Client > ")
s.send(msg.encode())
print("Server > ",s.recv(1024).decode())
```
# Server:

# Developed by: Lavanya S
# Register No: 212221220030
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
ClientMessage=c.recv(1024).decode()
c.send(ClientMessage.encode())
```
# OUTPUT :
# Client:

![image](https://github.com/LavanyaSIT/EX-8/assets/130207418/1d32deb6-9c8d-4be1-8493-d6a72466abc7)

# Server:
![image](https://github.com/LavanyaSIT/EX-8/assets/130207418/e2e6fbca-49ae-4cd4-a364-be4e776e156c)

# RESULT :

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.

