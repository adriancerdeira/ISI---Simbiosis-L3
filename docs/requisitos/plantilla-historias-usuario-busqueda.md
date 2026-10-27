# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Fecha | [dd/mm/aaaa] |
| Versión | [Versión de trabajo] |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Como usuario del sistema de cocina, quiero disponer de un motor de búsqueda flexible que me permita filtrar recetas por palabra o frase, por ingredientes incluidos o excluir ingredientes, para encontrar de forma rápida platos que se ajusten a mis necesidades, gustos y ingredientes que tengo disponibles.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

## Justificación de la división

La épica se ha dividido en tres historias de usuario porque cada una representa un criterio de búsqueda independiente que aporta un resultado útil y funcional por sí mismo desde su implementación. De este modo, el usuario obtiene valor inmediato ya sea explorando recetas por conceptos generales, aprovechando ingredientes disponibles o filtrando restricciones de fomra asilada.

## US-01

**Título:** Búsqueda por palabra o frase.

Como cocinero aficionado, quiero buscar recetas por palabra o frase, para descubrir platos relacionados con un concepto, tipo de cocina o nombre específico.

**Fuentes:** UR-08; UC-21; FR-085; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que el usuario se encuentra en la pantalla de búsqueda, cuando introduce el término "pasta" en el campo de texto libre, entonces el sistema muestra un listado de recetas que contienen la palabra "pasta" en su título o descripción.
- **CA-02.** Dado que el usuario se encuentra en la pantalla de búsqueda, cuando introduce una frase con errores menores de mayúsculas o espacios, entonces el sistema normaliza la cadena y devuelve los resultados coincidentes de igual manera.
- **CA-03.** Dado que el usuario introduce un término sin coincidencias en el sistema, cuando ejecuta la búsqueda, entonces el sistema muestra un mensaje claro indicando que no se encontraron recetas para esa palabra o frase.

## US-02

**Título:** Búsqueda por ingredientes incluidos.

Como usuario que desea aprovechar lo que tiene en la nevera, quiero buscar recetas seleccionando uno o varios ingredientes específicos que deben estar incluidos, para cocinar platos sin necesidad de comprar componentes adicionales.

**Fuentes:** UR-08; UC-21; FR-086; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que el usuario selecciona los ingredientes "tomate" y "queso" del catálogo, cuando ejecuta el filtro, entonces el sistema devuelve únicamente las recetas que contienen de forma obligatoria ambos ingredientes en su preparación.
- **CA-02.** Dado que el usuario selecciona varios ingredientes para su búsqueda, cuando visualiza los resultados, entonces el sistema prioriza y ordena las recetas que mejor se ajustan al listado de ingredientes seleccionados.
- **CA-03.** Dado que el usuario selecciona un ingrediente que no esta asociado a ninguna receta activa, cuando aplica el filtro, entonces el sistema notifica que no hay platos disponibles con ese ingrediente en este momento.

## US-03

**Título:** Búsqueda por exclusión de ingredientes.

Como persona con alergias alimentarias o preferencias en los ingredientes usados, quiero buscar recetas excluyendo ingredientes específicos de forma aislada, para obtener un listado de platos completamente seguros y aptos para mi consumo.

**Fuentes:** UR-08; UC-21; FR-087; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que el usuario marca el ingrediente "tomate" para excluir de manera aislada, cuando activa la búsqueda, entonces el sistema muestra todas las recetas de la base de datos excepto aquellas que contengan "tomate".
- **CA-02.** Dado que el usuario ha combinado una búsqueda de texto con la exclusión del ingrediente "gluten", cuando se procesa la consulta, entonces el sistema filtra los resultados de texto eliminando cualquier receta que incluya "gluten".
- **CA-03.** Dado que todas las recetas del sistema contienen un ingrediente que el usuario ha decidido excluir, cuando se ejecuta el filtro de exclusión, entonces el sistema muestra una pantalla vacía informando que no quedan recetas aptas tras aplicar la restricción.

## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |

## Dudas pendientes

[Cuestiones pendientes de aclaración. Si no quedan cuestiones, indicar «Ninguna».]
