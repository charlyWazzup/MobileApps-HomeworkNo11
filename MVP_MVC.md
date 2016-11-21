### Modelo Vista Presentador (Model View Presenter)

MVP es un patrón arquitectónico de interfaz de usuario diseñada para facilitar pruebas de unidad automatizada y mejorar la separación de inquietudes en lógica de presentación:

* El modelo es una interfaz que define los datos que se mostrará o no actuado en la interfaz de usuario.
* El presentador actúa sobre el modelo y la vista. Recupera datos de los repositorios (el modelo), y los formatea para mostrarlos en la vista.
* La vista es una interfaz pasiva que exhibe datos (el modelo) y órdenes de usuario de las rutas (eventos) al presentador para actuar sobre los datos.


### Modelo Vista Controlador (Model View Controler)

es un patrón de arquitectura de software, que separa los datos y la lógica de negocio de una aplicación de la interfaz de usuario y el módulo encargado de gestionar los eventos y las comunicaciones.

* El Modelo: Es la representación de la información con la cual el sistema opera, por lo tanto gestiona todos los accesos a dicha información, tanto consultas como actualizaciones.
* El Controlador: Responde a eventos (usualmente acciones del usuario) e invoca peticiones al 'modelo' cuando se hace alguna solicitud sobre la información.
* La Vista: Presenta el 'modelo' en un formato adecuado para interactuar 


La diferencia entre estos dos es que en el MVC el usuario interactua directamente con el Controlador. Este puede hacer peticiónes o consultas, mientras que en el MVP, el presentador solo recopila la información.