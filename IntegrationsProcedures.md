# Get started

## Que es realmente OmniStudio Integrations procedures?

Son aplicaciones usadas para leer y escribir data desde Salesforce y programas externos. Una Integration procedure puede ser llamada por un OmniStudio component:

* OmniScript
* FlexCard
* API
* Apex method

OmniStudio Integrations procedures es una programacion declarativa, todo se procesa del lado del servidor y hace multiples acciones en una sola llamada al servidor.

Explicaciones:

- Declarativo: Se usan elementos drag-and-drop para crear la estructura del proceso OmniStudio Integrations procedures
- Server-side processing: Mejora el performance
- Multiples actions in a single call.

Son utiles cuando:

- Se necesita acceso y transformar data de terceras partes
- No se requieren interacciones por parte del usuario
- Mover cargas de trabajo desde el cliente al servidor

### Ejemplos:

#### Integrations procedures manehja multiples Fuentes de informacion:

![Entradas de informacion]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-integration-procedures/get-started-omnistudio-integration-procedures/images/b1203ea97a8b9010862f7effa28e1e3a_ce-16-f-13-b-c-153-41-ba-b-112-211-c-92473788.png')

#### Integrations procedures entrega (Sirve) informacion para miuchas tecnologias

![Mutiples tecnologias para enviar]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-integration-procedures/get-started-omnistudio-integration-procedures/images/8c5a4a20c5fbda2c5e7cb3b666007b7a_7-db-51-f-97-24-c-7-4-c-4-e-9-dab-c-1152-a-2-f-99-c-4.png') 

#### Integrations procedures son portanbles

Una vez creadas se pueden usar en cualquier lugar

####  Integrations procedures reciben solo la informacion deseada

![Informacion deseada](Integrations procedure://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-integration-procedures/get-started-omnistudio-integration-procedures/images/bfac299c9660b6ee3ea98de98cf82490_7-aa-8-e-491-35-ef-43-aa-b-525-eaac-8431604-e.png')

1. Es la informacion recolectada
2. El filtro que aplicare para la informacion que llego
3. La informacion final

## Ventajas de las integrations procedures

Siempre se recomienda usarlo porque

- Da flexibilidad
- Hace las implementaciones mas faciles
- Mejora el performance de las FlexCards y OmniScript

Comparadas con los Apex codes

- Son mas faciles de mantgener y actualizar
- Toman menos del 97% de tiempo en desarrollar

# Integration procedure designer

## Integration procedure elements

Estos elementos no son visibles, son usados por detras para hacer sus operaciones. Y estos se dividen en dos grupos

### Groups

#### Chache Block

* Saves the output of the steps within it to a session or org cache for quick retrieval
* Stores frequently accessed and infrequently updated data, which saves round trips to the database and improves performance
* Allows data updates without caching
* Allows different cached data to expire at different times

#### Conditional Block 

Solo se ejecuta si se cumple una condicion

#### Loop Block

Itera sobre algunos elementos en un data array, habilitando opciones repetitivas sobre estos

#### Try-Catch Block

Es como un try execpt, se intenta algo y si falla se toma el error

![Grupos]('https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/omnistudio-integration-procedures/explore-omnistudio-integration-procedure-designer/images/3c51dfd4a34daa61d2ed59ce12be49a0_d-4-ef-4557-7214-4-cdf-8-aeb-0-c-337-fc-0-d-578.png')






