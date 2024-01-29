# Build a DataRaptor Turbo Extract

Como no hay una interfaz propia se deben usar ciertas tab en el editor de un DataRaptor para especificar que es un DataRaptor Turbo, espeficificamente:

- Extract tab
- Preview tab

## Extract Tab (Pestaña de Extracción):

En la pestaña Extract, se especifica la consulta que se realizará mediante DataRaptor en un objeto Salesforce (sObject).

- Se definen filtros para determinar los datos a recuperar del objeto.

- Se especifican los campos a extraer. En el ejemplo de Edit Account OmniScript, se extraen datos del objeto Account.

- Se configuran ajustes para recuperar datos del objeto Account, como el camino de salida y los campos a extraer.

En la pestaña Preview, se prueba la entrada y salida de DataRaptor utilizando parámetros de entrada y visualizando resultados.

## Preview Tab (Pestaña de Vista Previa):

Se prueba la entrada y salida de DataRaptor en la pestaña Preview.

Se especifica un par clave/valor en los parámetros de entrada, como AccountId y el RecordId de una cuenta.

Se visualizan los resultados en el panel de respuesta para confirmar la extracción correcta de datos.

## Build a DataRaptor Load (Construir una Carga de DataRaptor):

Para crear una carga de DataRaptor, se utilizan las pestañas 

- Objects
- Fields
- Preview 

En el DataRaptor Designer.

### En la pestaña Objects

Se especifican los objetos Salesforce que se actualizarán.

### En la pestaña Fields
Se mapea la entrada de datos a los campos del objeto Salesforce que se quieren actualizar.

### En la pestaña Preview
Se prueba la salida de DataRaptor al realizar cambios en el JSON de entrada.


## Create or Update: How Does a DataRaptor Load Decide? (Crear o Actualizar: ¿Cómo Decide una Carga de DataRaptor?):

Una carga de DataRaptor guarda actualizaciones en registros Salesforce, sobrescribiendo datos existentes o creando nuevos registros (upsert).

Es posible designar campos como Clave de Actualización `(Upsert Key)` para garantizar la coincidencia de registros únicos en Salesforce.

Se puede controlar el proceso de upsert seleccionando campos requeridos para la operación de upsert.

La carga de DataRaptor decide cómo guardar datos al verificar condiciones como la presencia de datos en campos requeridos para upsert y la coincidencia de claves de upsert con registros existentes en Salesforce.