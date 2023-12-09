# Enunciado
![Imagen01](01.png)
# Resolución

Al ejecutar el binario vemos que con una entrada grande ya se desborda y nos da una shell.
![](02.png)

Por lo que escribimos directamente el código con ayuda de las pwntools:

![](03.png)


~~~
from pwn import *
p = remote('10.10.6.214',9001)

payload = b'A'*200
p.recv()
p.sendline(payload)
p.interactive()
~~~
Veamos cada parte del código:

1. **`from pwn import *`**: Esta línea importa la biblioteca `pwn`. Esta biblioteca contiene funciones y clases útiles para escribir exploits y scripts de pruebas de penetración.

2. **`p = remote('10.10.6.214',9001)`**: Esta línea crea un objeto remoto que representa una conexión de red a la dirección IP `10.10.6.214` en el puerto `9001`, donde se está ejecutando la aplicación que se quiere explotar.

3. **`payload = b'A'*200`**: Aquí se crea una cadena de bytes (`payload`) que consiste en 200 caracteres "A". La letra `b` antes de `'A' indica que la cadena `'A'*200` debe ser tratada como una cadena de bytes en lugar de una cadena de texto normal (string) en Python.

En Python, las cadenas de texto (strings) y las cadenas de bytes son dos tipos de datos diferentes:

1. **String**: Representa texto. En Python 3, los strings se almacenan internamente como secuencias de caracteres Unicode. Son utilizados para trabajar con texto (por ejemplo, caracteres alfabéticos, dígitos, símbolos).

2. **Byte String**: Representa datos binarios. Se especifican con un prefijo `b` y se usan para trabajar con datos a nivel de byte, lo cual es útil para operaciones a bajo nivel, como la comunicación de red, el manejo de archivos binarios, y la seguridad informática (como en tu ejemplo).

Al usar `b'A'*200`, estamos creando una secuencia de 200 bytes, donde cada byte es un `0x41` (el valor ASCII de la letra 'A'). Esto es útil en el contexto de pruebas de penetración y explotación de vulnerabilidades, como buffer overflows, donde es importante tratar los datos como bytes puros en lugar de texto porque es importante tener un control preciso sobre la representación exacta de los datos que estás enviando.

4. **`p.recv()`**: Esta línea recibe datos del servidor. Es común en la comunicación de red esperar a que el servidor envíe algún tipo de mensaje o indicador antes de enviar datos. Esta función espera y recibe esos datos pero no los asigna a ninguna variable, ya que en este caso el mensaje del servidor no es relevante para el propósito del script.

5. **`p.sendline(payload)`**: Envía el `payload` al servidor. La función `sendline` envía los datos y luego una nueva línea, lo cual es común en la comunicación basada en texto.

6. **`p.interactive()`**: Finalmente, esta línea cambia la interacción con el servidor a un modo interactivo, permitiendo al usuario enviar comandos manualmente después de que se haya enviado el `payload`.


Lo ejecutamos y podemos acceder a la flag.

![](04.png)

 
**Autor:** [Andr3sdelRio](https://twitter.com/Andr3sdelRio) 

- [URL original del reto](https://tryhackme.com/room/pwn101) 
 

