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

![image](https://user-images.githubusercontent.com/95835522/180337819-f66718c1-085e-4c10-83f5-f5036492dc69.png)


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

## Ejercicio 6

### Soluciones de Salesforce

-  ***¿Qué es Salesforce?***
 
    Es una compañía de CRM que une empresas y clientes

- ***¿Qué es Sales Cloud?***

  Es una aplicación de Salesforce, basada en la nube, de CRM. Incluye herramientas para la gestión de contactos, la automatización de la fuerza de ventas, la previsión de ventas, así como la productividad.

- ***¿Qué es Service Cloud?***

  Es una solución completa de atención al cliente creada especialmente para dar soporte a los clientes a cualquier hora y en cualquier lugar

- ***¿Qué es Health Cloud?***

  Conecta sin problemas a los equipos de atención médica con una vista integral de cada paciente en una sola plataforma, que cumple con la HIPAA.
  
- ***¿Qué es Marketing Cloud?***

  es un proveedor de software y servicios de análisis y automatización de marketing digital.


### Funcionalidades de Salesforce

- **¿Qué es un RecordType?**

  Nos permiten definir diferentes Business Process, Pages Layouts y Picklist Values en un determinado objeto. Así mismo, los Record Types nos ayudan a mostrar distintos tipos de información según el perfil del usuario.
  
- **¿Qué es un ReportType?**

  Indica el tipo de informe al que pertenece la plantilla seleccionada previamente por el creador de la misma.

- **¿Qué es un Page Layout?**

  Los diseños de página controlan el diseño y la organización de botones, campos, s-controls, Visualforce, enlaces personalizados y listas relacionadas en páginas de registros de objetos.

- **¿Qué es un Compact Layout?**

  Un diseño compacto muestra los campos clave de un registro de un vistazo en la aplicación móvil Salesforce, Lightning Experience y en las integraciones de Outlook y Gmail.
  
- **¿Qué es un Perfil?**

  Los perfiles definen cómo acceden los usuarios a objetos y datos y qué pueden hacer en la aplicación.

- **¿Qué es un Rol?**

  Es aquella función que determina los niveles de acceso que tienen los usuarios.

- **¿Qué es un Validation Rule?**

  Las reglas de validación verifican que los datos que un usuario ingresa en un registro cumplen con los estándares que usted especifica antes de que el usuario pueda guardar el registro.

- **¿Qué diferencia hay entre una relación Master Detail y Lookup?**

  En lookup, ambos objetos no comparten propiedades entre ellos, lo que significa que están débilmente acoplados.
  
  En Master-detail, ambos objetos comparten propiedades entre sí, lo que significa que están estrechamente acoplados.

- **¿Qué es un Sandbox?**
  Un Sandbox es una copia de su organización en un entorno aislado que puede usar para distintos fines, como pruebas y capacitación.

- **¿Qué es un ChangeSet?**

  Un conjunto de cambios entrantes es un conjunto de cambios que se ha enviado desde otra organización de Salesforce a la organización en la que ha iniciado sesión. Un conjunto de cambios se debe implementar para que los cambios surtan efecto.

- **¿Para qué sirve el import Wizard de Salesforce?**

  Se puede utilizar para importar un máximo de 50,000 registros
  
- **¿Para qué sirve la funcionalidad Web to Lead?**

  Sirve para definir una campaña o fuente de clientes potenciales colocando valores dentro de los campos ocultos.

- **¿Para qué sirve la funcionalidad Web to Case?**

  Para ver cómo afectan al proceso de ventas., responder a casos satisface a sus clientes y mejora su marca.
  
- **¿Para qué sirve la funcionalidad Omnichannel?**

  Omni- canal es una función personalizable y flexible que se puede configurar de forma declarativa en Salesforce, es decir, sin necesidad de escribir código. OmniCanal ayuda al enrutamiento automático de diferentes tipos de elementos de trabajo (como casos y clientes potenciales) a los agentes.

- **¿Para qué sirve la funcionalidad Chatter?**

  Chatter facilita la conexión con las personas y la información que les es más relevante.

### Conceptos generales
- ¿Qué significa SaaS?

  El software como servicio (SaaS) es un modelo de entrega de software basado en la nube en el que el proveedor de la nube desarrolla y mantiene el software de las aplicaciones en la nube.
  
- ¿Salesforce es Saas?

  Salesforce es una compañía de PaaS (Plataforma como Servicio), un concepto que nace como resultado de la aplicación al desarrollo de Software del modelo SaaS (Software como Servicio). Este modelo abarca el ciclo completo para desarrollar e implantar aplicaciones desde Internet.

- ¿Qué significa que una solución sea Cloud?

  La computación en la nube (cloud computing) es una tecnología que permite acceso remoto a softwares, almacenamiento de archivos y procesamiento de datos por medio de Internet

- ¿Qué significa que una solución sea On-Premise?

  on-premise se refiere a que la instalación del programa se ha realizado de manera local, en las instalaciones de la empresa y obligando a esta a crear una infraestructura informática compleja con servidores que requieren mantenimiento.

- ¿Qué es un pipeline de ventas?

  El pipeline de ventas es, precisamente, el proceso de actividades y estrategias que necesita un vendedor para acelerar el ciclo de ventas, transformando clientes potenciales (aquellos que acaban de conocer tu marca o servicio) en clientes

- ¿Qué es un funnel de ventas?

  El concepto de embudo de ventas representa todo el proceso de cierre de un negocio, desde el momento de la captación hasta la conversión final.

- ¿Qué significa Customer Experience?

  El Customer Experience, también llamada experiencia del cliente o CX, es la experiencia que formará tu consumidor en función de sus interacciones con tu marca, que pueden ser positivas o negativas.

- ¿Qué significa omnicanalidad?

  Es una estrategia de comunicación utilizada para estar en contacto con los prospectos o clientes a través de diferentes canales (email, redes sociales, sitio web, etc.).

- ¿Qué significa que un negocio sea B2B?

  El término B2B nace de la expresión en inglés “business to business” (empresa a empresa). Es decir, son las ventas de una empresa a otra.

- ¿Qué significa que un negocio sea B2C?

  B2C es el acrónimo en inglés de “business to consumer” (empresa a consumidor). Es decir, es un modelo de negocio en el que una empresa le vende de forma directa al consumidor final.


- ¿Qué es un KPI?

  Un KPI, conocido también como indicador clave o medidor de desempeño o indicador clave de rendimiento, es una medida del nivel del rendimiento de un proceso. El valor del indicador está directamente relacionado con un objetivo fijado previa y normalmente se expresa en valores porcentuales.

- ¿Qué es una API y en qué se diferencia de una Rest API?

  Por lo general, la API sigue el formato de aplicación a aplicación, mientras que REST sigue una estructura diferente: Cliente-Servidor. El cliente y el servidor están evolucionando de forma independiente, proporcionando más flexibilidad en el trabajo.

- ¿Qué es un Proceso Batch?

  Los sistemas Batch se basan en la producción por lotes, que no es más que la producción de una cantidad limitada de un tipo de producto cada vez. Cada lote recibe una identificación, como número o código. Además, cada lote exige un plan de producción específico.

- ¿Qué es Kanban?

  La metodología Kanban es un sistema de producción tan eficiente como efectivo. Forma parte de las metodologías ágiles y su objetivo es gestionar la realización de las tareas hasta su finalización.

- ¿Qué es un ERP? 

  Enterprise Resource Planning (ERP) es un tipo de software que las organizaciones utilizan para gestionar las actividades empresariales diarias, como la contabilidad, el aprovisionamiento, la gestión de proyectos, la gestión de riesgos, el cumplimiento y las operaciones de la cadena de suministro.

- ¿Salesforce es un ERP? 

  Salesforce Billing complementa las plataformas de planificación de recursos de negocio (ERP) mediante la conversión de los datos de la gestión de procesos desde el prospecto hasta el pedido de Salesforce CPQ en datos de transacciones.

### Ejercicio 7
