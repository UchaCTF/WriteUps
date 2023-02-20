# Enunciado
I was trying to send a flag to my friend over UDP, one character at a time, but it got corrupted! I think someone else was messing around with me and sent extra bytes, though it seems like they actually abided by RFC 3514 for once. Can you get the flag?

Traducción: "Estaba tratando de enviar una bandera a mi amigo a través de UDP, un carácter a la vez, ¡pero se corrompió! Creo que alguien más estaba jugando conmigo y envió bytes adicionales, aunque parece que en realidad cumplieron con RFC 3514 por una vez. ¿Puedes conseguir la bandera?"

# Resolución

El RFC proporcionado se conoce como "The Security Flag in the IPv4 Header" y describe una bandera de seguridad en el encabezado IPv4, que se utiliza para indicar que un paquete IP es parte de un flujo de tráfico seguro. Es un RFC que no se ha adoptado ampliamente y actualmente se considera obsoleto.

Primero buscamos en la cabecera IP el flag con el bit al que hace rreferencia el RFC y, a continuación, buscamos un paquete que lo tenga marcado a 1 ya que en teoría, por el enunciado, ese es el tráfico que hay que descartar.

[01.png]

Una vez marcado, se puede hacer clic derecho en el campo e ir *Apply as filter->Selected*, para seleccionar el tráfico "ruidoso".
Después iremos a Edit-> Ignore all displyed, para ignorar dicho tráfico. En la pantalla principal quitamos el filtro que habíamos quitado y veremos lo siguiente:

[02.png]

Ahora solo tenemos que hacer clic derecho en cualquiera de los paquetes no ignorados e ir a *Follow -> UDP Stream:*

[03.png]
