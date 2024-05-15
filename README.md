# EXP: 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Client:
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server:
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUPUT:
### Client:
![307807052-4a2eb9f6-50c1-48fd-ac91-d96264deb03e](https://github.com/kanishka2305/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497357/7c089e2e-e07b-46c7-b6e2-c37e891d558a)


### Server:
![307807024-945eb049-dd59-41ec-beaf-bf89449d403d](https://github.com/kanishka2305/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497357/619061fc-53fa-46b0-9ac0-bcb303935c85)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
