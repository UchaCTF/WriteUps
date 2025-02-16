# Tracks

[página del reto](https://ctf.ehax.tech/challenges)

![imagen](https://github.com/user-attachments/assets/b9b6fd28-8984-4831-a938-dac130a20b62)

En este reto nos dan un vídeo de la intro de phineas y Pherb.
Con la ayuda de binwalk podemos extraer los archivos ocultos dentro de este
![imagen](https://github.com/user-attachments/assets/ba92eac2-5b97-44c9-b004-b1b907a6fbe4)

Dentro del archivo de vídeo, encontraremos un zip con contraseña con la flag dentro así como un qr.
![imagen](https://github.com/user-attachments/assets/198f7cf4-8873-4d37-ac70-1943c71d46ce)

A pesar de lo improbable que es el hecho de que escanear este qr nos ayude en algo, siempre es algo que podemos probar cuando estamos trabajndo en entornos controlados
En este caso, el qr contiene el texto "not every qr code should be scanned" lo que no es muy útil, pero puede ser una pista sonre la importancia de este qr.
![imagen](https://github.com/user-attachments/assets/6325e7ed-bfb3-4a4f-893a-8092b7ba7f64)

En este punto me puse a probar muchas herramientas para buscar datos ocultos dentro de este qr. Busque metadatos con exiftool, subí la saturación de la imagen, cambie colores...
Después de más horas de las que me gustaría admitir y con la ayuda de https://www.aperisolve.com/ (una página que aplica varias herramientas de esteganografía entre otras), terminé por encontrar datos relevantes
![imagen](https://github.com/user-attachments/assets/b9424f75-6835-4a2f-889f-bef6de2199cb)

Encontramos una posible flag EHAX{y04_ar3_6en!4$} junto a dos posibles contraseñas: $t@cy*1245 y $T@CY*1245
Ahora podemos probar las contraseñas en el zip a ver si logramos abrirlo

Abierto! pero este formato es un poco extraño.
![imagen](https://github.com/user-attachments/assets/f0115cda-7933-4a64-ba96-2b82daf19e3c)

Pense sería código cypher o parecidos. Finalmente, resulto ser código Vignere
![imagen](https://github.com/user-attachments/assets/e803365c-ceb4-471e-8eb7-6b350e9ae67b)
<details>
  <summary>Mostrar la flag</summary>
EH4X{d00fen$hmirt7_l0v3ed_$t4cy}
</details>

**Autor:** [Fernando Lorenzo](https://github.com/Fernandolv123)
