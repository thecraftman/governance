# Lanzamiento de métricas CHAOSS

El número de versión es `YYYY-MM` de la fecha de lanzamiento. Las contribuciones métricas continuas no obtienen un número de versión separado.

## Contribución métrica continua

El objetivo es tener ciclos cortos de retroalimentación y obtener métricas antes.

1. Coordinar el lanzamiento de la métrica a través de [la hoja de cálculo de seguimiento del lanzamiento](https://docs.google.com/spreadsheets/d/1tAGzUiZ9jdORKCnoDQJkOU8tQsZDCZVjcWqXYOSAFmE/edit#gid=0)

2. Decida en un grupo de trabajo que una métrica está lista para su lanzamiento.

3. Cree un problema de notas de la versión dentro del repositorio del grupo de trabajo y actualice la información para cada nueva métrica lanzada. Este problema se usará para crear las notas de lanzamiento de cadencia de lanzamiento regular.

4. Cree un problema para recopilar comentarios sobre esa métrica antes del lanzamiento.

5. Incluya un mensaje en el archivo de marcado de métrica que indique que la métrica será parte de la próxima versión regular. El mensaje debe estar en el archivo de reducción de métrica superior con el siguiente formato:

    ### Esta métrica es un candidato de publicación. Para comentar sobre esta métrica, consulte el [Problema #xx.](xxxxxxxxxxxxxxx) Después de un período de comentarios, esta métrica se incluirá en la próxima versión regular.

6. Agregue métrica a la página de métrica con una etiqueta "en revisión" y enlace al problema de comentarios.

7. Agregue un elemento en la página **Historial de versiones** en la sección *Contribuciones de métricas continuas desde la última versión* que indica que se agregó la métrica.

8. Anuncie la nueva métrica en la lista de correo y señale el problema y la página de rebajas para recibir comentarios. Actualizar comunidad en llamada de zoom semanal.

9. Dirija los comentarios en cuestión y mediante ediciones a la página de rebajas.

10. La métrica permanece en revisión hasta después del próximo lanzamiento regular

## Lanzamiento regular

La versión regular es cuando actualizamos el número de versión, actualizamos las notas completas de la versión y hacemos un gran anuncio. Estos lanzamientos ocurren una o dos veces al año y pueden corresponder con las fechas de CHAOSScon Norteamérica y Europa.

Cronología:

- 2 meses antes del lanzamiento
    - Decide una fecha de lanzamiento, coordina con grupos de trabajo
- 1 mes + 1 semana antes del lanzamiento
    - Finalice qué métricas incluir en el lanzamiento
    - Todas las métricas deben prepararse como el proceso de CMC descrito anteriormente
    - Agregue información en la página / métrica sobre el período de revisión y la fecha límite de lanzamiento planificada
    - Anuncie el **período de revisión** en la lista de correo
    - Los grupos de trabajo revisan y responden a los comentarios a medida que entran
    - Solicite reseñas en el boletín, Twitter, todas las llamadas de la comunidad durante el período de revisión
    - Grupos de trabajo redactan notas de la versión
- 1 semana antes del lanzamiento
    - Anuncie en la lista de correo que el período de revisión está cerrado
    - Prepare la versión final (ver más abajo)
        - Prepare el lanzamiento en PDF
        - Preparar notas de lanzamiento
        - Reemplazar / página de métricas con nueva versión
- Día de lanzamiento
    - Todo el trabajo fue hecho antes
    - Anuncie en la lista de correo y Twitter y todos los demás canales
    - ¡Celebrar!

### Prepara el lanzamiento final

- Determine el número de versión de lanzamiento porque se usará para varios pasos
- Amplíe la lista de contribuyentes para incluir a aquellos que contribuyeron a las versiones nuevas y anteriores
- Los grupos de trabajo responden a todos los comentarios en los temas y los cierran
- Los grupos de trabajo fusionan o cierran todas las solicitudes de extracción relacionadas con el lanzamiento
- Los grupos de trabajo eliminan la solicitud de revisión de la parte superior de todas las métricas
- Release Engineer crea una etiqueta de lanzamiento en todos los grupos de trabajo para congelar las métricas para el lanzamiento
    - Nombre de etiqueta: lanzamiento <versionnumber></versionnumber>
    - Descripción: notas de la versión para ese grupo de trabajo
- Release Engineer actualiza páginas métricas para extraer de la etiqueta de lanzamiento
- El ingeniero de versiones limpia `/metrics-rc` eliminando todo lo que no es necesario en la versión final
- Release Engineer transitions `/metrics-rc` a `/metrics` , reemplazando la versión anterior
- Release Engineer limpia la página de notas de la versión
- Release Engineer crea un PDF de la versión
- Release Engineer vincula el PDF en la página `/metrics` y las notas de la versión
