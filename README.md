# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE :03-05-2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM :

```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server
4.Send and receive the message using the send function in socket.
```
## PROGRAM :
```
Developed By: Yashaswi Mitta
Reg No: 212221230062
```
### client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server:
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
![cn 9-1](https://github.com/yashaswimitta/EX-9/assets/94619247/bdf45c82-0804-47e3-a8f8-d6365c59e52b)




## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.

