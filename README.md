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

Las Query String o cadenas de consultas es un término que se utiliza para hacer referencia a una interacción con una base de datos. Además, es la parte de una URL que contiene los datos que deben pasar a las aplicaciones web.

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


¿Cómo se envía la data en un Get y cómo en un POST?
¿Qué verbo http utiliza el navegador cuando accedemos a una página?
Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de
estructuras posibles.
Explicar brevemente el estándar SOAP
Explicar brevemente el estándar REST Full
¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?

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
