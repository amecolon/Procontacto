# América Colón | Evaluación práctica
## Ejercicio 1 Instalar aplicaciones

- IDE Visual Studio Code:

<p align="center">
  <img src="https://user-images.githubusercontent.com/95835522/178878567-b2b33b4d-4d6e-4ab8-bed2-059451e59f2c.png" />
</p>

- GIT y GIT Bash:

<p align="center">
  <img src="https://user-images.githubusercontent.com/95835522/178879767-c9f38bbd-0926-4684-8df3-3cdac058d08c.png" />
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

     Un sitio web que empieza con la URL http:// es entrado en un navegador web de la computadora del cliente.

     El navegador envía un request al servidor web que está hospedado en el website.
   
     El servidor web regresa una respuesta como un página de HTML, o algún otro formato de documento al navegador
    
     El navegador despliega el response del servidor al usuario. 

¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?
¿Qué es un queryString? (En el contexto de una url)
¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?
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
