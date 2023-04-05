# VishwaCTF2023
    
  

  ![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/0.png)
  
  
## JUST FILES

  



### Solución
    
    
    vishwaCTF{lucifer_S01E03}
  
  
### Análisis

Descargamos los archivos y tenemos dos imágenes.

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/6.png)

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/7.png)

Extraemos metadatos y no vemos nada relevante así que tiramos de steghide para encontrar archivos ocultos.

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/1.png)

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/8.png)

Encontramos un archivo oculto en la primera imagen que nos cuenta que aquí no hay nada y que deberíamos comprobar la segunda imagen en la cual encontramos un archivo de audio.

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/2.png)

Analizamos con Audacity el archivo en el que escuchamos un código morse al principio y luego lo que parece un diálogo al reves.

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/3.png)

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/4.png)

Valiendonos del modo revert para intentar entender la conversación descubrimos que es un fragmento de la serie lucifer siendo este el personaje que tenemos que adivinar.

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/5.png)

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/9.png)

![](https://github.com/albertominan/WriteUps/blob/1528ade3e5a700bbb3298c09ba6aeceb4b4b4e53/Esteganograf%C3%ADa/VishwaCTF2023/JUSTFILES/capturas/10.png)


**Autor:** [AlbertoMiñan](https://github.com/albertominan)
