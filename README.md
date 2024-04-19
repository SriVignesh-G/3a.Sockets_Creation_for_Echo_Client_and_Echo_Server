# Ex No:3a CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# Name: Sri Vignesh G
# Reg No: 212223040204
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
### Client.py:
```
import socket
s=socket.socket()
s.bind(('localhost',9000))
s.listen(5)
c,addr=s.accept()
while True:
    clientMessage=c.recv(1024).decode()
    c.send((clientMessage.encode()))

```
### Server.py:
```
import socket
s=socket.socket()
s.connect(('localhost',9000))
while True:
    msg=input("client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUTPUT:
### Client Window:
![Screenshot 2024-04-19 230703](https://github.com/SriVignesh-G/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147576510/06c09cd1-ceff-42e6-8154-92bbe3253783)

### Server Window:
![Screenshot 2024-04-19 230708](https://github.com/SriVignesh-G/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147576510/e4cdd19a-72b0-4e13-ab98-ea3a3a44e547)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
