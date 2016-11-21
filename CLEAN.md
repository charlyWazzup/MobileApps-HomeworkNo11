### ¿Qué es la CLEAN architecture?

Es una arquitectura que describió _Uncle Bob_ en su blog. 

![CLEAN](https://8thlight.com/blog/assets/posts/2012-08-13-the-clean-architecture/CleanArchitecture-8b00a9d7e2543fa9ca76b81b05066629.jpg)

Los círculos concéntricos representan diferentes áreas del software. En general, cuanto mas nos alejemos del núcleo mayor es el nivel del software. Los círculos exteriores son mecanismos mientras que los interiores son políticas. La regla primordial que hace que esta arquitectura funcione es la regla de dependencia. Esta regla dice que las dependencias a nivel de código fuente sólo pueden apuntar hacia dentro. Nada que se encuentre en un circulo interior puede saber algo sobre lo que hay en un círculo exterior. Particularmente, algo declarado en un círculo externo no puede ser mencionado desde el código situado en un círculo interno. Eso incluye funciones, clases, variables o cualquier otra entidad software. Por la misma razón, los formatos de datos usados en un círculo exterior no deberían usarse por un círculo interior, especialmente si esos formatos son generados por algún framework en un círculo situado al exterior. No queremos que nada de un círculo exterior impacte en los círculos o niveles interiores.

#### Entidades

Las entidades encapsulan la lógica de negocio de la empresa. Una entidad puede ser un objeto con métodos, o puede ser un conjunto de estructuras de datos y funciones. 

#### Casos de Uso

Estos casos de uso dirigen el flujo de datos hacía y desde las entidades y hacen que las entidades usen su lógica de negocio empresarial para conseguir el objetivo del caso de uso.

#### Interface Adapters

El software de esta capa es un conjunto de adaptadores que convierten datos desde el formato mas conveniente para el caso de uso y entidades al formato mas conveniente o aceptado por elementos externos como la base de datos o la web.

#### Frameworks y Drivers

El círculo o capa más externa se compone generalmente de frameworks y herramientas como la base de datos, el framework web, etc. Normalmente en esta capa sólo se escribe código que actúa de pegamento con los círculos o capas interiores. En esta capa es donde van todos los detalles.  La web es un detalle. La base de datos es un detalle. 