# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

# DATE:15-03-2023

# AIM :

To write a python program to perform stop and wait protocol


# ALGORITHM :

1.Start the program.

2.Get the frame size from the user

3.To create the frame based on the user request.

4.To send frames to server from the client side.

5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.

6.Stop the program

# PROGRAM :

## CLIENT :

Developed by :SHARANGINI T K

Register Number :212222230143
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
```
## SERVER :

Developed by :SHARANGINI T K

Register Number :212222230143

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Received".encode())
```

# OUTPUT :

## CLIENT :

![image](https://github.com/shara56/EX-2/assets/113497104/02b7cdaf-1109-453c-8fb9-52fa99bfa0f6)

## SERVER :

![image](https://github.com/shara56/EX-2/assets/113497104/8188a38d-426d-433c-8767-b47944a74d82)


# RESULT :

Thus, python program to perform stop and wait protocol was successfully executed.



