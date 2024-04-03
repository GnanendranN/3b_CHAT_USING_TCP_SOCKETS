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
### Client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
### Server
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
## OUPUT
### Client
![image](https://github.com/GnanendranN/3b_CHAT_USING_TCP_SOCKETS/assets/138955207/88c3f39f-31fd-43b2-b15a-19987945a65d)
### Server
![image](https://github.com/GnanendranN/3b_CHAT_USING_TCP_SOCKETS/assets/138955207/242fd123-908c-42f4-8286-e370b01c990b)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
