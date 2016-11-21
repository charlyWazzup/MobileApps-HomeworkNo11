### �Qu� es la CLEAN architecture?

Es una arquitectura que describi� _Uncle Bob_ en su blog. 

![CLEAN](https://8thlight.com/blog/assets/posts/2012-08-13-the-clean-architecture/CleanArchitecture-8b00a9d7e2543fa9ca76b81b05066629.jpg)

Los c�rculos conc�ntricos representan diferentes �reas del software. En general, cuanto mas nos alejemos del n�cleo mayor es el nivel del software. Los c�rculos exteriores son mecanismos mientras que los interiores son pol�ticas. La regla primordial que hace que esta arquitectura funcione es la regla de dependencia. Esta regla dice que las dependencias a nivel de c�digo fuente s�lo pueden apuntar hacia dentro. Nada que se encuentre en un circulo interior puede saber algo sobre lo que hay en un c�rculo exterior. Particularmente, algo declarado en un c�rculo externo no puede ser mencionado desde el c�digo situado en un c�rculo interno. Eso incluye funciones, clases, variables o cualquier otra entidad software. Por la misma raz�n, los formatos de datos usados en un c�rculo exterior no deber�an usarse por un c�rculo interior, especialmente si esos formatos son generados por alg�n framework en un c�rculo situado al exterior. No queremos que nada de un c�rculo exterior impacte en los c�rculos o niveles interiores.

#### Entidades

Las entidades encapsulan la l�gica de negocio de la empresa. Una entidad puede ser un objeto con m�todos, o puede ser un conjunto de estructuras de datos y funciones. 

#### Casos de Uso

Estos casos de uso dirigen el flujo de datos hac�a y desde las entidades y hacen que las entidades usen su l�gica de negocio empresarial para conseguir el objetivo del caso de uso.

#### Interface Adapters

El software de esta capa es un conjunto de adaptadores que convierten datos desde el formato mas conveniente para el caso de uso y entidades al formato mas conveniente o aceptado por elementos externos como la base de datos o la web.

#### Frameworks y Drivers

El c�rculo o capa m�s externa se compone generalmente de frameworks y herramientas como la base de datos, el framework web, etc. Normalmente en esta capa s�lo se escribe c�digo que act�a de pegamento con los c�rculos o capas interiores. En esta capa es donde van todos los detalles.  La web es un detalle. La base de datos es un detalle. 