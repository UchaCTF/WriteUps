# Be The Admin
## Enunciado

https://2023.squarectf.com/challenge?Be%20The%20Admin

![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/716d3ec2-070c-43d9-baa6-7005ffdf6e61)

## Resolución

Primero de todo debemos conectarnos a la web para ver que se nos ofrece. Dentro de esta encontraremos dos ids relacionados a dos nombres.

![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/067fade1-b886-4d30-b0fa-ed8a676a95a2)
![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/9b4157de-1585-4a1f-8aed-259a5fb905f9)

Si accedemos a las cookies, encontraremos una cookie “session_id” con su correspondiente valor.
![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/fc5636db-71ce-4992-b75d-4762b412fb75)

Podemos copiar este valor y buscarlo en alguna bases de datos para ver si encontramos alguna correspondencia.
![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/c3d838df-50cd-469b-881f-bf4a153babb8)
![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/64f2de25-01e3-40af-85cf-8417aa08f6c1)

sabiendo que la cookie es un base64 de CTF Participant (el mismo nombre que uno de los usuarios mostrados en la web), podemos convertir “Admin” a base64 y cambiar el valor de session_id por este.
![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/c245c7c8-63a4-45e8-b6a9-c737706ea040)

Haciendo cambios a la cookie finalmente acabé encontrando la flag oculta eliminando el símbolo ‘=’ en la sesión.
![imagen](https://github.com/Fernandolv123/ExamenPrimera/assets/98803514/47d464ed-c3b4-4153-a86b-b4705611af90)

``flag{boyireallyhopenobodyfindsthis!!}``





**Autor:** [Fernando Lorenzo](https://github.com/Fernandolv123)
