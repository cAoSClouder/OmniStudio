# Work with Child FlexCards

Porque son importantes los ChildFlexCards

1. Las ChildFlexCards son reutilizables
2. Ayuda a recuperar informacion de diferentes ubicaciones y mostrarla en una sola
3. Son usadas como Flyouts (Menus desplegables)

Para que sea considereda como ChildFlexCard, previamente se debio haber configurado como una ChildFelx card.

![FlexCard elements]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards-building-and-publishing/work-with-child-flexcards/images/54b63c401a4789cf8ded6a7791320a80_517-b-8-c-9-f-b-390-47-ec-8-e-7-f-63-b-64842-ea-06.png' )

1. Nombre de la FlexCard
2. Data node field. Involicra el paso de informacion desde el objeto padre al objeto hijo.

### Colaose a Block

![Collapse block]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards-building-and-publishing/work-with-child-flexcards/images/6b0d9fe053eca065597feb610a82252b_94-f-0-b-499-3-e-38-4-d-69-b-59-e-7-d-30-a-7926-d-66.png')

Un bloque que colapsa es el que se encoge o expande desde la flecha, dependiendo de las configuracion seleccionada

## Pasar Records o Data de un padre a un hijo

![ChildFelxCardConfig]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards-building-and-publishing/work-with-child-flexcards/images/d9d9e409338da23a1aec0d85222f82ad_42-f-8-db-88-482-e-4-d-0-f-9362-2399-b-40-ae-58-d.png')

1. Primero seleccionar el elemento en el que se mostrara la informacion del hijo
	- En "Properties-FlexCard Name" se coloca el nombre de la flex card hija 
2. Es donde se selecciona la informacion disponible para enviar al objeto hijo, cuando se selecciona
	- {record} : Se envia la informacion actual al hijo
	- {recirds] : Envia toda la informacion

## Pasar data a un hijo

Si se quiere pasar informacion especifica a un hijo se usa el *Attributes property*.
Solo se le debe ingresar y asignar el valor.


# Build a FlexCard with External Data

Fuentes externas de datos incluyen

- Legacy data sources
- On-premises
- API integrations
- Other third-party data and applications

API's de clima son muy usadas en las industrias

## Display data in a Flyout

A flyout can display

- Informacion de textos largos que no encajan en la estructura estandar de las FlexCards
- Informacion de los registros hijos

Hay tres tipos de flyouts:

- Child FlexCards
- OmniScript
- Custom Lightning web component (LWC)


Ejemplo:

![Ejemplo FlexCard](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards-building-and-publishing/build-a-flexcard-with-external-data/images/165ce5860917e1a1b09ce2a5abafbd17_bdd-9-c-97-e-95-f-7-4-bf-6-9-cd-3-4595-fcacf-95-f.png' )
    
To create this flyout, you configure the Action element like this:

*  Action Type: Flyout
*  Flyout Type: Child Card
*  Flyout: Select the activated child FlexCard to use as the flyout
*  Open Flyout In: Modal

Como se esta manejando informacion externa se debe de tener en cuenta que el Data Source type es **Integration Procedures**


# Add FlexCard States and COnditions

## Display data using multiple FelxCard states

Todas las flex cards se crean con estado. El estado de una FlexCard controla que puede ver un usuario y que hace con la FlexCard. En un caso simple una FlexCard puede tener:

- Un estado activo si hay informacion para mostrar

Es decir, supongamos que se tienen dos FlexCards

1. Muestra la fecha de vencimiento de la Poliza de seguro
2. Muestra el formulario para renobarla si se encuentra vencida

La segunda no se mostrara si la primera no esta vencida. Esto es un estado


- Un estado en blanco o abierto si no hay informacion o acciones limitadas.

Es decir, supongamos que se tienen 3 FlexCards

1. Despliega informacion del plan 
2. Despliega informacion del vencimiento del plan
3. Es una FlexCard(Con estado **Abierto**)  el cual posibilita la creacion de un plan

## Cloning a State and Configuring Display Conditions

En la parte superior derecha, aparece el simbolo de clonar.

Se da la opcion de al clonar, colocar las condiciones para copiar.

## The navigate Action

La accion de navegacion direcciona a los usuarios desde las FlexCards hacia paginas web externas, paginas lightning experience y lightning comunities.

![Nagivate settings]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards-building-and-publishing/add-flexcard-states-and-conditions/images/0dfb0fa0b9482e39327fd22265c83c2e_ef-4-ecbad-bcb-5-4-ff-1-8713-2-c-9-cd-7-b-869-dc.png')

## Version a FlexCard

Versionar es una forma de hacer cambios a la FlexCard mientras se mantiene la FlexCard existente.

### Cuando versionar y cuando Clonar

1. Versionar
	- Cuando se quieren hacer ligeras modificaciones en una FlexCard existente y probar su comportamiento
	- Cuando se quiere actualizar una FlexCard
2. Clone a FlexCard
	- Cuando se quiere una FlexCard independiente de su padre
	- Cuando se quiere cambiar el nombre o autor de la FlexCard

# Activate and publish FlexCards

Una vez creada la FlexCard esta crea un  Lightning web componet (LWC) que puede ser publicado en una Lighting o Community page.
t

Para esto se deben configurar las "Publish options" 

![Publish options]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-flexcards-building-and-publishing/activate-and-publish-flexcards/images/9080eefc6b470facbeeff52d4d245778_picture-201.png' )

Hay las siguientes opciones de publicacion.

1. Master label: Esta es el nombre visible de la FlexCard

2. API ersion: Esta es el API version de la FlexCard

3. Runtime Namespace: El nombre del paquete administrado

4. Is exposed: Se activa cuando se quiere que el paquete este publicado.

5. Add SVG: Se usa para agregar un icono SVG

6. Targets: Estos son los sitios donde se espera que la flex card sea publicada
	- App Page
	- Home Page
	- Record Page
	- Community Page
	- Community Default

## Add a FlexCard in a Lighting o Experence page

En ambos casos la FlexCard aparece en la seccion de componentes.

Para activar Standar OmniStudio Runtime

1. Clik on the gear
2. *OmniStudio Settings*
3. Standard OmniStudio Runtime

![Arquitectura]('/home/cesar/Pictures/FlexCardArquitecture.png')




# FlexCards conditional styles

Se sua para notificar algo, esto depende del cumplimiento de cierta condicion

# Notas

- Siempre se debe habilitar el OmniScript support, si se van a trabajar con un LWC.
- Se debe registrar un *Event listener* que es el que caturara los elementos seleccionados en este caso.


























