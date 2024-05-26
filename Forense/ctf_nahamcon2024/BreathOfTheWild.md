# Breath of the Wild Writeup

[página del reto](https://ctf.nahamcon.com/challenges)

El reto nos da un archivo comprimido, una contraseña, y nos pregunta donde fueron descargadas las imagenes que contiene.
![6db53abd-fe54-4338-9dd3-a24746546b85](https://github.com/UchaCTF/WriteUps/assets/98803514/a25979cb-aa58-4724-bf18-372020429294)


primero de todo, descargaremos y descomprimiremos el archivo.
El archivo resultante, no tiene extension, esto no presenta un gran problema, ya que simplemente abriendolo con un editor de texto plano, podemos descubrir el tipo de archivo
![25fa4a53-9d7d-4a0a-a4c4-33fa19df3761](https://github.com/UchaCTF/WriteUps/assets/98803514/71b3407c-f204-446b-99dc-75ae717cbb81)

Siendo  este un archivo vhdx (disco duro virtual)

En una mágina virtual, podemos montar este archivo para ver su contenido
![20fff060-ab93-4f20-9a4f-7d142948a21e](https://github.com/UchaCTF/WriteUps/assets/98803514/255cf878-8b13-4302-a6c6-87163163eec6)

Dentro, podemos encontrar una gran cantidad de imagenes, resaltando la número 46, ya que el nombre del disco es el de este juego
![064b22d0-2b13-45c2-89f7-6428f17ee2f4](https://github.com/UchaCTF/WriteUps/assets/98803514/c93a0afe-9381-4941-b331-e508213d906a)

A partir de estas imagenes, probé a buscar dentro de sus metadatos usando la página jimpl a ver si encontraba alguún dato de relevancia
![imagen](https://github.com/UchaCTF/WriteUps/assets/98803514/ad4ee8f0-f2ce-4c7e-8e6d-ba81e876fc04)

Pero no encontre nada interesante.
Al no encontrar nada importante, probé suerte usando FTKImager, aprovechando que ya tengo el disco montado.
Tras montar la imagen, me dirigí a esta imagen.
![1c05a05f-a6f2-46b9-ae19-bbbb6e794c6e](https://github.com/UchaCTF/WriteUps/assets/98803514/f6572b8d-e537-4820-a9d1-f7b589858e32)

Encontrando la web de descarga junto a sospechosa cadena html.

Como podemos ver en la siguiente captura, la página existe, pero la url ha sido alterada

![ec18d7ca-a52c-4cd8-93be-69f0f52e343f](https://github.com/UchaCTF/WriteUps/assets/98803514/53911246-d520-4ebf-9576-25755ab3468b)
Por lo que el siguiente paso es la decodificación de esta cadena, para ello utilicé la página CyberChef

![38bb3cae-bc10-470c-8aa2-093977fc0604](https://github.com/UchaCTF/WriteUps/assets/98803514/c6b6ebdc-5719-41fa-aff8-f04a7e9df925)

<details>
  <summary>Mostrar la flag</summary>
flag{83f2b0a8ce39f2e5ba1d6c70e97f291e}
</details>

**Autor:** [Fernando Lorenzo](https://github.com/Fernandolv123)
