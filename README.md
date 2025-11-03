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
### SERVER 
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
### CLIENT 
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
### SERVER

<img width="1481" height="915" alt="image" src="https://github.com/user-attachments/assets/5acbbdc7-3b7a-4464-a1b0-67e855c04987" />

### CLIENT 

<img width="1476" height="912" alt="image" src="https://github.com/user-attachments/assets/98e553da-154a-4f58-b005-42f372ad1aff" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
