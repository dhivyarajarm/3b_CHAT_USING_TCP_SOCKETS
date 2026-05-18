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
##Sever side
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
## client side
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
<img width="1202" height="573" alt="Screenshot 2026-05-15 153955" src="https://github.com/user-attachments/assets/ec119471-a07a-435d-bf1f-f64557b734b4" />
<img width="1165" height="636" alt="Screenshot 2026-05-15 154013" src="https://github.com/user-attachments/assets/92edcc63-8886-4fd7-be0a-f513f95fa2cf" />
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
