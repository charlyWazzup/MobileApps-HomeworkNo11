### �Qu� es EventBus?

Es es una herramienta cuya finalidad es la de lanzar y capturar eventos entre diferentes clases. Est� basada en el patr�n bus de eventos y su implementaci�n consiste en que uno o varios objetos se suscriben a un canal a trav�s del cual escuchan, y otro, en el momento en el que suceda algo que desea notificar, lanza un evento a trav�s de este canal y todos aquellos que estaban escuchando reaccionar�n haciendo aquello que ten�an programado al suscribirse a �ste.

EventBus no solo nos facilita la tarea de notificar a los suscriptores acerca del evento si no que nos permite enviar informaci�n asociada a ese evento a trav�s del canal y decidir en qu� hilo se ejecutar� la respuesta.

#### Ventajas

* Flexbilidad
	Con EventBus se pueden realizar numerosas funcionalidades, incluso generar toda una forma de trabajar basada en estos eventos. 

* Simplicidad
	En solo tres sencillos pasos ya podemos hacer uso de esta herramienta. 
	
* Agilidad
	Ahorramos muchas l�neas de c�digo, clases y l�gica de interacci�n que, al fin y al cabo, se traduce en un menor tiempo de desarrollo. 

#### Desventajas

* Un bus de eventos no es un canal de comunicaci�n, sino una forma de notificar eventos entre los suscriptores y los generadores; por lo que su finalidad no es la de servir como herramienta de paso de mensajes.

* Un error muy com�n es el de estar suscrito a muchos eventos y controlar qu� evento es el que se est� recibiendo en funci�n de la informaci�n que se nos env�a. Los datos asociados al evento contienen informaci�n complementaria a este, y no para distinguirlo de otro. 

* Hay que tener cuidado, no tanto de en qu� hilo se lanzan los eventos, sino en el de la respuesta; ya que, por defecto, �stas se ejecutan en el mismo hilo en el que se lanza el evento.
