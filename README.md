# 3b.CREATION FOR CHAT USING TCP SOCKETS

## Developed By : SANJAY M
## Register No  : 212223230187

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:

## client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```

## server.py
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
## OUTPUT:
## client:
![Screenshot 2024-04-11 144052](https://github.com/sanjayofficial2005/3b_CHAT_USING_TCP_SOCKETS/assets/148048602/67ed1970-0a58-4566-b5b0-bb11ab5fe476)

## server:
![Screenshot 2024-04-11 144103](https://github.com/sanjayofficial2005/3b_CHAT_USING_TCP_SOCKETS/assets/148048602/7fb967e6-9e36-4a79-b24b-930aeee1ee25)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
