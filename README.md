# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Developed By:sakthivel M
### Register No: 212222240088
## Server Side:
```python
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## Client Side:
```python
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## OUTPUT:
![out 3a](https://github.com/Sakthimurugavel/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/118707246/f5d4a310-2b29-4e2e-9941-34fa6eeb3fb1)

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
