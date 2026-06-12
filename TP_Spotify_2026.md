# Trabajo Práctico Spotify

## Introducción

El objetivo de este trabajo es realizar un análisis exploratorio de un dataset de Spotify. El mismo contiene el historial de reproducciones de un usuario de Spotify. El dataset se encuentra en el archivo `StreamingHistory_Extended.csv`.

Para realizar el análisis, se debe utilizar Python y las herramientas vistas en clase. En particular Pandas y Matplotlib. Opcionalmente se pueden utilizar otras herramientas como Seaborn.

Se va a evaluar la calidad del análisis realizado, la presentación de los resultados y la claridad de las conclusiones obtenidas. Ademas se tendrá en cuenta la calidad y prolijidad del código utilizado, se espera que el las variables sean tipadas, que se utilicen nombres de variables descriptivas y que el código esté comentado

## Consigna

El análisis tiene que incluir los siguientes puntos:

1. ¿Que información contiene el dataset? Describir las columnas y los tipos de datos. Pista: ¿Son todas las columnas necesarias para el análisis? ¿Son todos los registros del mismo tipo?
2. ¿A partir de que fecha se registraron las reproducciones? ¿Hasta que fecha?
3. ¿Cuántas canciones diferentes se escucharon en total?
4. ¿Cuánto es la duración total de las reproducciones de canciones registradas? Pista: ¿Alguna columna del dataset indica la duración de la reproducción?
5. ¿Cuál es el artista más escuchado por tiempo total de reproducción?
6. ¿Cuál es la canción más escuchada por tiempo total de reproducción?
7. Del artista más escuchado (por tiempo reproducido), ¿cuál es la canción más escuchada?
8. Determinar el top 10 de artistas más escuchados . Elegir un tipo de gráfico adecuado para visualizar los resultados.
9. Determinar el top 10 de canciones más escuchadas. Elegir un tipo de gráfico adecuado para visualizar los resultados.
10. Además se deben plantear al menos 3 análisis adicionales. Responderlas utilizando el dataset y acompañarlas con gráficos adecuados.

## Bonus

- ¿Cuál es el día de la semana en el que más se escucha música? ¿Y el horario del día?
- ¿Cuál es el mes en el que más se escucha música?
- ¿Cuál es el artista que más se escucha en cada mes?
- ¿Cual es la canción más veces salteada?

## Bonus 2

Utilizando la API de Spotify a traves de la libreria [`spotipy`](https://spotipy.readthedocs.io/en/2.24.0/) obtener información adicional de las canciones y/o artistas. Por ejemplo, se puede obtener el género de la canción, una sample de 30 segundos de la canción, imagen de portada para usar en las visualizaciones, etc. Ademas se puede solicitar por cada cancion un set de "audio_features" que incluye información como la _energía_, el _tempo_, y la _danceability_ de la canción entre otros. Sugerencia, no solicitar la información de todas las canciones del dataset, ya que la API de Spotify tiene un límite de requests por minuto. Solicitar solo de algunas canciones como por ejemplo las 10 canciones más escuchadas.

## Algunas consideraciones a tener en cuenta

- Cada registro corresponde a una reproducción, y contiene un campo `ms_played` que indica la duración de la reproducción en milisegundos. Por lo tanto, se debe tener en cuenta este campo para determinar la canción más escuchada.
- Al explorar el datasets, se deben "limpiar" los datos antes de visualizar los DataFrames. ¿Todos los registros son de Canciones? ¿Hay valores nulos?
- Para responder a las preguntas, se debe ademas generar visualizaciones que permitan entender mejor los datos. Por ejemplo, se puede generar un gráfico de barras para visualizar el artista más escuchado. Investigar la documentación de Matplotlib para generar distintos tipos de gráficos.
- Al determinar, por ejemplo, la canción más escuchada, se debe tener en cuenta que una misma canción puede aparecer varias veces en el dataset (Ojo, hay nombres de canciones repetidos en canciones distintas. Pensar en como resolver esto).
- Se pueden utilizar datos agrupados por mes, día de la semana, etc. Investigar la documentación de Pandas para convertir las fechas al tipo de dato `datetime` y como se puede extraer el mes, día de la semana, etc. de una fecha. Recomendación, crearse nuevas columnas en el DataFrame con esta información.

## Entrega

El análisis se hace completando el archivo `analisi.ipynb`. Debe tener bloques de código pero también bloques de texto sacando conclusiones y explicando lo que se hace.

Rodas las celdas deben estar ejecutadas.

## Condiciones de entrega

El notebook debe ejecutarse sin errores y debe incluir:

- Una explicación de los pasos realizados y las conclusiones obtenidas.
- Las visualizaciones generadas.
- El código utilizado para responder a las preguntas y para generar las visualizaciones.

## Referencias

- [Documentación de Pandas](https://pandas.pydata.org/docs/)
- [Documentación de Matplotlib](https://matplotlib.org/stable/contents.html)
- [Documentación de Seaborn](https://seaborn.pydata.org/)
- [Documentación de Python 3](https://docs.python.org/3/)