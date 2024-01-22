# Capacidades claves de las Flex cards

FlexCards display contextual information in an at-a-glance format and provide access

FlexCards muestra información contextual en un formato de un vistazo y brinda acceso a tareas relevantes para los datos mostrados.



- FlexCards summarize contextual information at a glance.
    - ![Sumarice]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards/discover-the-key-capabilities-of-flexcards/images/cb50bd05dbe5d4fff79bed8ea393377a_0-f-0-fceca-1-ad-2-4589-886-b-f-6-e-1-bd-628035.png')
- FlexCards are the beginning and ending points for customer transactions.

- FlexCards are viewable on any device or channel.
- FlexCards can display data from multiple data sources.
- FlexCards are built quickly using drag-and-drop elements.
- FlexCards have a what-you-see-is-what-you-get (WYSIWYG) editor for controlling their layout and style.
- FlexCard actions are relevant to the context of the card.
- FlexCards are embeddable in other FlexCards.
- FlexCards are embeddable inside an LWC OmniScript.
- FlexCards display more detail on demand with flyouts.
- FlexCards have multiple states that display based on conditions.

## Header and cambas

### Header

Es donde se ven meta datos basicos como lo son : Autor, Version, Si es hija de otra FelxCard, etc.


### Canvas

El cambas es donde se alojan los elementos:
	- Imagenes
	- Acciones
	- Stados
	- child FlexCards

## Build, properties, style, and Setup Panel

Para construir las FelxCards se necesita drag fields y elementos al canvas

- Fields: Campos necesarios segun la configuracion

### Build

![PantallaPrincipal]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards/explore-the-flexcard-designer/images/706c4f9065b164d2c71e8ae4d48ba71b_mycasedetails-style.png')


Es donde se encuentran los Campos y los Display

- Fields
	- Elementos
- Display
	- Acciones
	- Bloques
	- Graficos

### Properties Panel

Cuando se agrega un elemento al canvas, se despliegan las propiedades de este 


### Style panel
Se usa para actualizar la apariencia de una FlexCard (Se le puede agregar un propio CSS)

### Setup panel
Se usa para configurar 

* Update your Data Source.
* Apply custom permissions to limit access to your FlexCard.
* Track Custom Data on elements with tracking enabled.
* Enable Multi-Language Support, set Session Variables, and create Event Listeners

## Previw and Publish

Se puede ver una Preview y se puede activar.

### Previw

Se puede cambiar el tipo de vista (Diferentes dispositivos), Se pueden agregar Testeo, Y Inyectar codigo JSON


![Previw]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards/explore-the-flexcard-designer/images/dd793758626443bc3a21052a84b607cf_mycasedetails-preview.png' )


# Asistente de datos

## Create FlexCard

Estos son los pasos que ofrece el asistente

![Pasos del asistente de creacion de las FLexCards]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards/meet-the-data-source-wizard/images/b766d8c2bd51782aac965655588fb391_3-b-5-cd-92-a-cd-7-d-4-b-86-a-785-c-0-d-3-c-6279714.png' )

1. Definir la FlexCard

En este paso se modifican configuraciones basicas como:

- Autor
- Titulo
- Nombre
- Descripcion
- Si es una FelxCard Child
- Tema 
	- Lightning
	-  Newport

2. Definir la estructura de datos

La estructura define la forma en la que la FelxCard recupera la informacion. Esto se puede actualizar siempre se necesite.

Estas son algunas

* Apex REST uses a REST endpoint of an Apex class to return data.
* Apex Remote uses an Apex Remote class and method to return data.
* Custom uses sample JSON to set up a FlexCard with temporary data that will eventually be replaced with another data source.
* SOQL Query uses the Salesforce Object Query Language (SOQL) to search an org’s Salesforce data for specific information. For example, SELECT Name, Id FROM Account LIMIT 5.
* SOSL Search uses the Salesforce Object Search Language (SOSL) to construct text-based search queries against the search index.
* Streaming API uses the Salesforce Streaming API to send notifications of general events that are not tied to Salesforce data changes.
* SDK uses a method from a Software Development Kit (SDK) to get data to populate fields on a FlexCard.

You can also use OmniStudio data tools.

* DataRaptor uses a DataRaptor Extract interface to return data from a Salesforce object.
* Integration Procedures uses an Integration Procedure to return data from multiple internal and external s

3. Definir la estrucuta de datos

Como se define "Integration procedure", se definen las varaibles para pasar por la integracion

4. Definir las entradas de datos 

"Configure inputs" permite hacer test sobre las variables, estos test retornan un JSON con la informacion recolectada

# Display Data and Actions on a FlexCard

## FlexCard Elements

- Block elements: Estos combinan grupos de elementos logicos dentro de una flexcard
	- Se pueden colocar bloques dentro de bloques
	- Se pueden hacer elementos que colapsen para que se puedan deplegar
- Text and Field elements
	- Text: Se pueden usar, campos de texto plano, rich text o text rich que permite editar con HTML
	- Fields: Tiene dos formas
		* La simple que es agregar un elemento de texto 
		* Tomar un elemento editandole la salida

- Icono: Despliega una variedad de iconos predefinidos
- Menus and actions elements: 
![Menus y acciones]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards/display-data-and-actions-on-a-flexcard/images/5fb96422ae16a9b00311e952a28ab91d_e-7-a-04660-39-ad-4375-b-178-6-b-606-b-7-fb-81-b.png' )

Estos pueden tener diferentes acciones como	



# Style flexCards elements

## Caracteristicas del estido de panel

Se usa para arreglar el "CSS" de los elementos, algunos especificos son

* Action
* Datatable
* Field
* Icon
* Menu
* Togglee

## Enable responsiveness

Se debe activar para que varie el Responsibe dependiendo del dispositivo. Por defecto inicia en lo mas small posible

## Save and apply styles

En la pesatana de Style aparece una flecha en la cual se puede guardar el estilo creado



# FelxCards Sta# FelxCards States

1. State 1 - conditions
	Can hide elements depends of the conditions
2. State 2 - No conditions
3. State 3 - Blank Card State (no records returned))

# FelxCards actions

![Actions](/home/cesar/Pictures/FelxCardsActions.png)
