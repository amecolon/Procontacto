# América Colón | Evaluación práctica
## Ejercicio 1 Instalar aplicaciones
  
<p align="CENTER">
  <img src="https://user-images.githubusercontent.com/95835522/179066249-ef885dfe-397d-405b-b5e3-bbd409849a22.png" />
</p>

## Ejercicio 2 Conceptos estándar

### SERVIDOR HTTP

Un servidor web se define como un software que hace uso del HTTP _(Hypertext Transfer Protocol)_ para almacenar los archivos que forman los sitios web y mostrarlos a los usuarios cuando estos lo solicitan.

> Algunas empresas, cuentan con un servidor web propio. No obstante, en la gran mayoría de ocasiones, tanto particulares como compañías, optan por contratar este servicio a un proveedor de alojamiento web.


### VERBOS HTTP

*GET*

- Solicita una representación de un recurso específico. Las peticiones que usan el método GET sólo deben recuperar datos.

*HEAD*
-  Pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta.

*POST*
- Se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.

*PUT*
- Reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.

*DELETE*
- Borra un recurso en específico.

*CONNECT*
- Establece un túnel hacia el servidor identificado por el recurso.

*OPTIONS*
- Es utilizado para describir las opciones de comunicación para el recurso de destino.

*TRACE*
- Realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.

*PATCH*
- Es utilizado para aplicar modificaciones parciales a un recurso.


### Request y response en HTTP
  HTTP se basa en un modelo solicitud / respuesta, La comunicación de datos empieza con un request enviado del cliente, y termina con la respuesta del servidor web.

Veamos un ejemplo:

- Un sitio web que empieza con la URL http:// es entrado en un navegador web de la computadora del cliente.
- El navegador envía un request al servidor web que está hospedado en el website.
- El servidor web regresa una respuesta como un página de HTML, o algún otro formato de documento al navegador 
- El navegador despliega el response del servidor al usuario. 
     
Los HTTP headers son la parte central de los HTTP requests y responses, y transmiten información acerca del navegador del cliente, de la página solicitada, del servidor, etc

<p align="CENTER">
  <img src="https://user-images.githubusercontent.com/95835522/179069851-bc0595fa-e8ce-4292-a252-1b51725184f2.png" />
</p>

### QueryString

- Las Query String o cadenas de consultas es un término que se utiliza para hacer referencia a una interacción con una base de datos. Además, es la parte de una URL que contiene los datos que deben pasar a las aplicaciones web.

### ResponseCode

Los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica.

1. Respuestas informativas (100–199)
2. Respuestas satisfactorias (200–299)
3. Redirecciones (300–399)
4. Errores de los clientes (400–499)
5. Errores de los servidores (500–599)

### Data en GET y POST

*GET*

Con el método GET, los datos que se envían al servidor se escriben en la misma dirección URL. En la ventana del navegador. Toda la información introducida por el usuario (los llamados “parámetros URL”) se transmiten tan abiertamente como el URL en sí mismo. Esto tiene ventajas y desventajas.

*POST*

El método POST introduce los parámetros en la solicitud HTTP para el servidor. Por ello, no quedan visibles para el usuario. Además, la capacidad del método POST es ilimitada.

| | GET | POST |
|---| ----- |----- |
| Visibilidad | Visible en la barra de direcciones para el usuario | Invisible para el usuario|
| Marcadores e historiales de navegación | Los parámetros URL se guardan junto al URL | Los parámetros URL no se guardan junto al URL |
| Caché y registro del servidor	| Los parámetros URL se guardan sin cifrar. | Los parámetros URL no se guardan automáticamente |
| Comportamiento al actualizar el navegador o retroceder | Los parámetros URL no se envían de nuevo | El navegador advierte de que los datos del formulario se enviarán de nuevo | 
| Tipo de datos | Solo caracteres ASCII | Caracteres ASCII y datos binarios |
| Longitud de datos | Limitado al máximo del URL (2048 caracteres) | Ilimitado |

- **¿Qué verbo http utiliza el navegador cuando accedemos a una página?**

    Se utiliza el verbo GET

### Estructuras de datos JSON y XML

*JSON*

  Las siglas JSON se corresponden con ***JavaScript Object Notation***, presenta la información de una manera más legible para las personas. Se basa en un subconjunto concreto del lenguaje de programación JavaScript con la aplicación de una serie de pares de nombre y valor e, incluso, por una lista de valores en orden.

  A nivel estructural, este protocolo de intercambio de datos se distingue por el uso de llaves. Además, cada nombre que se incluye en el formato va seguido de dos puntos. Si te fijas en elementos de la misma rama del árbol, te encontrarás con que todos están separados por una coma.

      { 
        "persons": [ 
          { 
            "name": "Ford Prefect", 
            "gender": "male" 
          }, 
          { 
            "name": "Arthur Dent", 
            "gender": "male" 
          }, 
          { 
            "name": "Tricia McMillan", 
            "gender": "female" 
          }
        ]
      }


*MXL*

  Una de las claves para el éxito de este formato es que su estándar se basa en texto, con el objetivo de ofrecer una representación adecuada de todo tipo de información estructurada, por ejemplo, en datos o documentos.

  El XML se basa en el uso de etiquetas. Estas pueden ser vacíos o tener contenido y otros elementos. Siempre se encuentran entre <> y se cierran con </>. En este estándar también se encuentran atributos, una herramienta muy eficaz para añadir propiedades a un elemento. Existe la posibilidad de que las etiquetas tengan uno o más de uno para complementar su valor.

      <xjson> 
        <object> 
          <name>persons</name> 
          <value> 
            <array> 
              <object> 
                  <name>name</name> 
                  <value>Ford Prefect</value> 
                  <name>gender</name> 
                  <value>male</value> 
              </object> 
              <object> 
                  <name>name</name> 
                  <value>Arthur 
                  Dent</value> 
                  <name>gender</name> 
                  <value>male</value> 
              </object> 
              <object> 
                  <name>name</name> 
                  <value>Tricia McMillan</value> 
                  <name>gender</name> 
                  <value>female</value> 
              </object> 
            </array> 
          </value> 
        </object> 
      </xjson>


## SOAP
La comunicación en Internet se basa principalmente en protocolos como HTTP, HTTPS, FTP o, a otro nivel, TCP. Pero SOAP es esencial para los servicios web, interfaces a través de las cuales un dispositivo puede hacer uso del servicio de un servidor. Los buscadores, las tiendas en línea y otros muchos servicios en Internet funcionan a través de dichos servicios web, y SOAP es uno de los protocolos que lo hacen posible.

SOAP posibilita la comunicación entre un cliente, como el navegador de Internet, y los servicios de un servidor. Para que esto sea posible, el cliente debe enviar una solicitud a la API. El framework de SOAP determina la forma que debe adoptar dicha solicitud. Dentro de esta definición de la solicitud también pueden incluirse datos específicos de la aplicación, lo que es un punto fuerte de SOAP. De esta forma, los servicios web pueden desplegar aplicaciones diferentes. Para que puedan utilizarse como servicios web sin necesidad de tener la misma sintaxis.

<p align="CENTER">
  <img src="https://user-images.githubusercontent.com/95835522/179086833-af143873-84df-4bfd-8462-9bc173cbcace.png" />
</p>


### RESTFUL

- Una API de REST, o API de RESTful, es una interfaz de programación de aplicaciones (API o API web) que se ajusta a los límites de la arquitectura REST y permite la interacción con los servicios web de RESTful. El informático Roy Fielding es el creador de la transferencia de estado representacional (REST).

### Headers en un request

- Los headers en un request contienen toda la información básica de la petición, a la espera de una RESPONSE

### Key Content-type en un header

_Content-Type_ es la propiedad de cabecera (header) usada para indicar el  media type (en-US) del recurso. _Content-Type_ dice al cliente que tipo de contenido será retornado.
> En solicitudes (tales como POST o PUT), el cliente indica al servidor que tipo de dato es enviado actualmente.

    Content-Type: text/html; charset=utf-8
    Content-Type: multipart/form-data; boundary=something

## Ejercicio 3

Instalación

![image](https://user-images.githubusercontent.com/95835522/178880442-e09d27ac-499e-49d4-b319-5d5f8d80ad5f.png)

Paso 1:

![image](https://user-images.githubusercontent.com/95835522/178883414-28cce583-6634-42b5-8b03-a07b3fa1c987.png)

Paso 2:

![image](https://user-images.githubusercontent.com/95835522/178883460-e0915082-eb10-4ee7-830a-b17ef42ac7d7.png)

Paso 3:

![image](https://user-images.githubusercontent.com/95835522/178883523-9847fdb5-edfb-4856-8b42-7f4facef700b.png)

¿Qué diferencias se observan entre las llamadas el punto 1 y 3?
En el primero no aparecian mis datos y en tercero despues de hacer un post y regresarlo ya estoy dentro de la base de datos.

## Ejercicio 4

### Módulos de Trailhead

Link del perfil público:

https://trailblazer.me/id/amecolon

## Ejercicio 5

### Conceptos

| Nombre | Concepto | 
| ------ | ------- | 
| Lead | Representa un prospecto o cliente potencial.  |
| Account | Representa una cuenta individual, que es una organización o persona involucrada con su negocio (como clientes, competidores y socios). |
| Contact | Representa un contacto, que es una persona asociada a una cuenta. |
| Opportunity |  Representa una oportunidad, que es una venta o trato pendiente. |
| Product | Productos son los elementos y servicios que distribuye a clientes. Cada producto puede existir en múltiples listas de precios con precios diferentes |
| PriceBook | Es una lista de productos y sus precios |
| Quote | Representa una cotización, que es un registro que muestra los precios propuestos para productos y servicios.  |
| Asset | Representa un artículo de valor comercial, como un producto vendido por su empresa o un competidor, que ha comprado un cliente. |
| Case | Representa un caso, que es un asunto o problema del cliente. |
| Article | Los artículos de conocimientos son documentos de información. Los artículos pueden incluir información sobre procesos, como cómo restablecer su producto a sus valores predeterminados o preguntas más frecuentes.|

### Diagrama

<p align="CENTER">
  <img src="https://user-images.githubusercontent.com/95835522/180331391-236d7291-a3c6-4228-a31b-57e6cca7f1a4.jpg" />
</p>


