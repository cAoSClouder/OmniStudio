# Arquitectura de OmniStudio

## Introduccion


Caoas de componentes de OmniStudio:

### Digital Experience
Esta incluye dos componentes principales de una intefaz de usuario

- OmniStudio FlexCards: Tarjetas que muestran informacion y acciones en un formato de vistazo para los datos de cuentas de clientes
- OmniScripts: Una ruta guiada para completar el proceso de negocios

### Service Management
Incluyen servicios de datos que leen, escriben, transforman, calculan y rastrean datos dentro y fuera de salesforce

- OmniStudio DataRaptors: Son servicios configurables para recuperar, transformar y actualizar datos.
- Procedimientos de integracion de Omnistudio: Procesos que ejecutan multiples acciones en una sola llamada al servidor.

### Developer experience
Es una capa del ciclo de vida de la aplicacion con herramientas que permiten que los desarrolladores gestionen y transfieran cambios de componentes de OmniStudio entre distintos entornos.

- IDX Build Tool: Herramienta de atomatizacion de la linea de comandos que empaqueta y migra los paquetes de datos de OmniStudio en un formato apto para el control de fuentes
- IDX Workbench: Aplicacion de escritorio que los desarrolladores migren paquetes de datos y metadatos de Salesforce 

### Ejemplos

Supongamos que un cliente se comunica con un centro de llamadas para actualizar su domicilio y verificar otros detalles de la cuenta.

A través de una pantalla de integración de telefonía computarizada (CTI), el agente del centro de llamadas inicia una página de la consola donde se muestra información sobre el cliente que llama y su cuenta. La página muestra una serie de **FlexCards**

 Un **procedimiento de integración (abreviado “IP” en las imágenes a continuación)** conectado a las FlexCards hace llamadas de API al sistema de facturación y, luego, muestra los datos en una **FlexCard de “Billing Data”** (Datos de facturación). Mientras tanto, otro procedimiento de integración hace una llamada de API a un sitio web del clima y muestra la temperatura actual (54 °F o 11° C) en la ubicación del cliente.

Cada FlexCard tiene diferentes acciones relevantes para sus datos. Una de estas acciones es iniciar un proceso para actualizar el domicilio de un cliente, que actualmente es 1234 Main St. Any City, State 01234. Al hacer clic en esta acción, se abre una página modal con pasos y pautas para cambiar el domicilio. Se trata de un **OmniScript**.
 La mayoría de los detalles de domicilio están previamente rellenados, gracias a que **DataRaptor Extract**  extrae estos datos del objeto Cuenta de Salesforce. Cuando el agente cambia el domicilio a 456 Second Street, Any City, State 01236 y completa el proceso guiado, una instancia de **DataRaptor Load** guarda los cambios modificados de vuelta en el objeto Cuenta.

## Digital experience

La capa de experiencia digital ofrece la experiencia interactiva para los usuarios.

[Digital Experience](#digital-experience)

### FlexCards

Resumen la informacion basica de un vistazo, Una Consola de interacción de OmniStudio muestra una vista integral de la cuenta y la información de un cliente. Las FlexCards son componentes de estas vistas integrales. La consola en sí es una consola Salesforce Lightning.

### OmniScripts

Ofrece a los clientes una ruta guiada para completar un proceso de negocios.

Supongamos que un cliente quiere hacer lo siguiente:

- Ver y actualizar su información de contacto, que está almacenada en Salesforce.
- Ver su plan de servicio, que está almacenado en la base de datos heredada.
- Ver su factura, que se encuentra en un sistema de facturación, optar por pagarla y seleccionar una forma de pago específica.

Para hacer todo esto, un agente inicia procesos guiados desde **Flex cards**

### Componentes web lightning de Salesforce (LWC)

Son se activan Flex cards o OmniScrips, estos pasan a ser LWC, estos:

- Funcionan dentro de comunidades y portales
- Ajustan sus dimensiones para procesarse correctamente en el navegador o telefono

## Service Management
La capa de gestion de servicios incluye los servicios que **leen, escriben, transforman, calculan y rastrean datos dentro y fuera de Salesforce**

[Servicios](#service-management)

### Datas Raptors

Es una herramienta de asignacion que permite leer, transformar y escribir datos de Salesforme

Hay 4 tipos de DataRaptors:

##### Dataraptor turbo
Obtener datos de un unico objeto de Salesforce

####  Dataraptor extract
Obtener datos de uno o mas objetos de salesforce 

####  Dataraptor Load
Guarda datos en uno o mas objetos de Salesforce

####  Dataraptor Transform
Manipula los datos provenientes de dentro o fuera de Salesforce

### Procedimientos de integracion
Son una forma de recuperar, guardar y manipular datos en segundo plano. Tambien para procesar datos complejos de diversas fuentes

Motivos:

- La mayoria de casos en el servidor se procesan mas rapido
- Combina varias acciones en una sola llamada al servidor
- Minimisa las llamadas de cliente/servidor


