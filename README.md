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
### CLIENT:
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
### SERVER:
```python
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
### client
![3b1](https://github.com/Aakash0407/3b_CHAT_USING_TCP_SOCKETS/assets/118799103/9b7c6c44-0940-4baa-869c-488abbaf27f5)

### server
![3b2](https://github.com/Aakash0407/3b_CHAT_USING_TCP_SOCKETS/assets/118799103/8bc120a6-a9b7-4b20-9ee1-17ae0a9a6b4b)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
