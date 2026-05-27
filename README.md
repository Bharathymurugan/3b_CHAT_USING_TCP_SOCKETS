# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
Client 
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

 Server
 import socket
s=socket.socket()
s.bind(('localhost',8005))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
 ```
## OUTPUT
Client

<img width="546" height="144" alt="Screenshot 2026-05-27 055430" src="https://github.com/user-attachments/assets/a26508f9-0d80-4a48-acee-b753c91566c7" />

Server

<img width="600" height="153" alt="Screenshot 2026-05-27 055443" src="https://github.com/user-attachments/assets/6d462f60-7c11-479a-b094-7c277110aaab" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
