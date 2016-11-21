### Modelo Vista Presentador (Model View Presenter)

MVP es un patr�n arquitect�nico de interfaz de usuario dise�ada para facilitar pruebas de unidad automatizada y mejorar la separaci�n de inquietudes en l�gica de presentaci�n:

* El modelo es una interfaz que define los datos que se mostrar� o no actuado en la interfaz de usuario.
* El presentador act�a sobre el modelo y la vista. Recupera datos de los repositorios (el modelo), y los formatea para mostrarlos en la vista.
* La vista es una interfaz pasiva que exhibe datos (el modelo) y �rdenes de usuario de las rutas (eventos) al presentador para actuar sobre los datos.


### Modelo Vista Controlador (Model View Controler)

es un patr�n de arquitectura de software, que separa los datos y la l�gica de negocio de una aplicaci�n de la interfaz de usuario y el m�dulo encargado de gestionar los eventos y las comunicaciones.

* El Modelo: Es la representaci�n de la informaci�n con la cual el sistema opera, por lo tanto gestiona todos los accesos a dicha informaci�n, tanto consultas como actualizaciones.
* El Controlador: Responde a eventos (usualmente acciones del usuario) e invoca peticiones al 'modelo' cuando se hace alguna solicitud sobre la informaci�n.
* La Vista: Presenta el 'modelo' en un formato adecuado para interactuar 


La diferencia entre estos dos es que en el MVC el usuario interactua directamente con el Controlador. Este puede hacer petici�nes o consultas, mientras que en el MVP, el presentador solo recopila la informaci�n.