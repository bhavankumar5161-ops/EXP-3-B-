# 3b.CREATION FOR CHAT USING TCP SOCKETS:
### REGISTER NUMBER = 212225240026
## DATE = 14.2.2026

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
# server:
~~~
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
~~~
## Client:
~~~
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
~~~

## OUPUT:

<img width="960" height="606" alt="Screenshot 2026-02-14 111957" src="https://github.com/user-attachments/assets/f664b904-6bd1-4ef3-8c07-06854d0d7f13" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
