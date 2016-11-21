### ¿Qué es EventBus?

Es es una herramienta cuya finalidad es la de lanzar y capturar eventos entre diferentes clases. Está basada en el patrón bus de eventos y su implementación consiste en que uno o varios objetos se suscriben a un canal a través del cual escuchan, y otro, en el momento en el que suceda algo que desea notificar, lanza un evento a través de este canal y todos aquellos que estaban escuchando reaccionarán haciendo aquello que tenían programado al suscribirse a éste.

EventBus no solo nos facilita la tarea de notificar a los suscriptores acerca del evento si no que nos permite enviar información asociada a ese evento a través del canal y decidir en qué hilo se ejecutará la respuesta.

#### Ventajas

* Flexbilidad
	Con EventBus se pueden realizar numerosas funcionalidades, incluso generar toda una forma de trabajar basada en estos eventos. 

* Simplicidad
	En solo tres sencillos pasos ya podemos hacer uso de esta herramienta. 
	
* Agilidad
	Ahorramos muchas líneas de código, clases y lógica de interacción que, al fin y al cabo, se traduce en un menor tiempo de desarrollo. 

#### Desventajas

* Un bus de eventos no es un canal de comunicación, sino una forma de notificar eventos entre los suscriptores y los generadores; por lo que su finalidad no es la de servir como herramienta de paso de mensajes.

* Un error muy común es el de estar suscrito a muchos eventos y controlar qué evento es el que se está recibiendo en función de la información que se nos envía. Los datos asociados al evento contienen información complementaria a este, y no para distinguirlo de otro. 

* Hay que tener cuidado, no tanto de en qué hilo se lanzan los eventos, sino en el de la respuesta; ya que, por defecto, éstas se ejecutan en el mismo hilo en el que se lanza el evento.
