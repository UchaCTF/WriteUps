# Enunciado
*A magician made the seven wonders disappear. But people claim they can still feel their presence in the air.*

**Traducción:** "Un mago hizo desaparecer las siete maravillas. Pero la gente afirma que aún puede sentir su presencia en el aire."

# Resolución

El fichero es un jpg que muestra siete maravillas del mundo. 

![Imagen01](havealook.jpg)

Mirando con exiftool no aparece ningún metadato interesante, por lo que vamos a utilizar binwalk para ver si hay algún fichero oculto.

![](01.png)

Vemos que sí. Tenemos un fichero de audio. Lo vamos a abrir con audacity y mirar su espectro (despegable izquierdo):

![](02.png)

Bingo!

Flag: vishwaCTF{n0w_y0u_533_m3}
 
**Autor:** [Andr3sdelRio](https://twitter.com/Andr3sdelRio) 
