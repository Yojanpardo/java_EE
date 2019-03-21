# Java EE
Este repo es mi agenda para las notas del curso de Java EE de platzi.  
  
Es una version de Java enfocada en el sector empresarial y va a servir para hacer aplicaciones web, al final del curso vamos a realizar una REST API que podremos implementar en nuestras páginas web y móviles.  
  
Estaremos haciendo uso del modelo vista controlador.  
  
Java EE nace porque se necesitan aplicaciones distribuidas transaccionales y portables que usan todas las capacidades de un servidor.  
  
## Servidores
Para un proyecto de estos se hace necesario el uso de un servidor que sirva para almacenarlo y poder acceder a él. Existen diferentes servidores entre los cuales encontramos los siguientes:

### De pago 

* WebLogic
    _Oracle_   
* JBoss Enterprise Application Platform
    _Red Hat_
* WebSphere
    _IBM_ 

### Gratuitas

* JOnAS
    - _ObjectWeb_
* Wildfly
    - _Versión de JBoss por la comunidad_
* GlassFish
    - _Oracle_
* Gernónimo y TomEE
    - _Apache_

### Apache TomCat
No es considerado un servidor de aplicaciones, es un contenedor de aplicaciones y es para trabajo exclusivo con Java Servlets

## JSP
Java Server Pages, son las páginas compuestas de html, js y css, a demás puede contener código de java, para poder ejecutarlo necesitamos tener apache tomcat instalado.

## Servelet
Es una clase que hereda métodos de la clase HttpServlet, una vez heredados tiene la capacidad de manejar cualquier tipo de request, para identificarlo puedes ubicar dentro del código sus métodos doGet o doPost o atraves de su anotación (@WebServlet) + el nombre que le quieras dar como URL.

## BEAN 
Sirven para modelar un objeto con sus atributos y métodos, sus propiedades deben ser accesibles por getters y setters y deben ser serializables para permitir el acceso a ellos a traves de peticiones http.

## MVC
Podemos utilizar el Modelo Vista Controlador para generar nuestros proyectos en java en donde veremos que la vista está dada por el HTML o los archivos JSP, los modelos estarán dados por nuestras clases de java y los controladores son nuestros BEANs.  
Para estos primeros intentos voy a hacer el repositorio de [hola_mundo_jsp](https://github.com/Yojanpardo/hola_mundo_jsp.git) en donde muestro mi primer pequeño proyecto con JSP.

## WAR
Es el tipo de empaquetado utilizado por Java EE para desplegar aplicaciones web sin tener que exponer el código que hemos creado.  
Para crear este empaquetado debemos ir a nuestro IDE, hacemos clic derecho sobre nuestro proyecto, le damos clic en exportar->WAR file y luego lo ponemos en producción en nuestro servidor importando nuestro WRA file.

## Asistentes inteligente Maven
Los asistentes insteligentes nos ayudan a trabajar sobre plantillas para facilitar el trabajo, descargar librerias de terceros, cerar todos los componentes y archivos ejecutables.  
Maven es un asistente inteligente que nos va a ayudar a hacer todo a partir de XML ya que describe el proyecto a construir, Dependencias, Compilación del código y Empaquetado.  
De esta manera nosotros como desarrolladores solo tendremos que enfocarnos en la creación del código y no perder tiempo haciendo estas tareas tan repetitivas.

## Gradle
Está basado en Groovy que es un lenguaje orientado a objetos y usa la sintaxis Domain Specified Language - Json
~~~
static mapping = {
    table 'person'
    columns {
        name column:'name'
    }
}
~~~
Esto debe ir en un archivo llamado build.gradle
que va a contener las dependencias, compilación del código y empaquetado.

## Aplicaciones orientadas a presentacion vs servicios
Los proyectos tradicionales son orientados a presentación pero necesitamos hacer una aplicacion orientada a servicios para poder desarrollar una Rest API  en la cual se va a cambiar la esquematización de un proyecto y poder accesarlo desde una página web o una aplicación movil de una forma más sencilla.

## Spring Toll Suite
Es el nuevo IDE que utilizaremos para la creación de nuestro proyecto, viene con la integración de Maven, creado por la comunidad SpringSource.  
Para descargar este IDE debemos dirigirnos a la [página de Spring](https://spring.io/tools) 