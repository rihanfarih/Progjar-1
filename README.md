# Progjar-1

Tugas 1.

Buat client-server yang mengimplementasikan, perintah:

py namafile.py server 127.0.0.1
py namafile.py client 127.0.0.1

> ping hallooo woorldddddd ....
terima : hallooo woorldddddd ....

> ls
ws_tcp.py

> ls /etc/*
passwd
group
....

> get /etc/passwd passwd2
fetch:/etc/passwd size: 2341 lokal:passwd2

> get /etc/passwd abc
fetch:/etc/passwd size: 2341 lokal:abc

> quit
server shutdown..
client shutdown..

Hari ini:

*) variable length paket 
 
nanti saya share filenya...

*) gunakan modul glob

import glob
glob.glob("C:/TMP/*")

*) gunakan perintah file I/O

f = open("/etc/passwd", "rb")
b = f.read()
print(len(b))
f.close()

b = open("/etc/passwd", "rb").read()
f = open("/etc/passwd2", "wb+)
c = bytes(b, "ascii")
f.write(c)
f.close()

*) input user

cmd = input("> ")
cmds = cmds.split()
if cmds[0]=="ls":
    print("ls")
elif cmd[0]=="get":
    print("get")
elif cmd[0]=="quit":
    print("quit")
else:
    print("unknown...")

*) sleep()

import time
time.sleep(1)


> tahapan..

client -> input()
split()
if cmd[0]=="ls":
   send(len_cmd+cmd)
   recv(3)
   b = recv(len_msg)
   print(repr(b))


server ->
   receive(3)
   cmd = receive(len_msg)
   split()
   if cmd[0] == "ls":
       buf = glob.glob[cmd[1]]
       send(len_buf+buf)
   

