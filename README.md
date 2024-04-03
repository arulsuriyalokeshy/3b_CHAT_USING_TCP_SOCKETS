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
Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```

Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## OUPUT
Server:

![image](https://github.com/arulsuriyalokeshy/3b_CHAT_USING_TCP_SOCKETS/assets/149130151/7901f4bc-1354-4ac0-8270-9169977084bc)



Client:

![image](https://github.com/arulsuriyalokeshy/3b_CHAT_USING_TCP_SOCKETS/assets/149130151/4be7d971-c3a5-4300-a4ed-66923195e7f3)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
