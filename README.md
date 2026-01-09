# Introducción

Desde el año 2010, la Policía Municipal de Madrid ha registrado información detallada sobre todas las personas implicadas en los accidentes intraurbanos de la ciudad.

En este proyecto se presentan las hipótesis de partida, el análisis exploratorio de los datos y las conclusiones derivadas de los datasets correspondientes
a los últimos cinco años, proporcionando una visión integral de los factores asociados a la siniestralidad y su evolución temporal, geográfica y demográfica.

El objetivo general de este EDA es determinar qué variables influyen de manera más significativa en la siniestralidad y la lesividad de los accidentes intraurbanos en la ciudad de Madrid, así como analizar la relación entre ambas, con el fin de aportar evidencia que permita reducir la accidentalidad y mejorar la seguridad vial urbana. Los objetivos específicos son: 

1. Analizar los accidentes en Madrid desde una perspectiva temporal, geográfica y demográfica, evaluando la influencia de factores asociados y su relación con la lesividad, para identificar periodos, zonas y condiciones de mayor riesgo.
2.	Establecer posibles relaciones bivariantes y multivariantes entre variables, para identificar patrones y asociaciones relevantes para la seguridad vial.
3.	Proporcionar recomendaciones basadas en los resultados, priorizando intervenciones en los periodos, zonas y situaciones de mayor riesgo.

**Hipotesis planteadas**

- Los meses, días de la semana y horas con mayor número de accidentes podrían ser enero, los lunes y las 8:00 de la mañana, respectivamente.
- La franja horaria de mayor siniestralidad podría corresponder a la mañana (06:00–12:00).
- Los distritos céntricos de Madrid presentan un mayor número de accidentes en comparación con los distritos periféricos.
- Los jóvenes de 18 a 29 años podrían ser el grupo etario más implicado en accidentes.
- Los hombres presentan mayor frecuencia de accidentes que las mujeres, y la mayoría de los implicados en los siniestros son conductores.
- El turismo es el tipo de vehículo más implicado, y la colisión lateral podría ser el tipo de accidente más frecuente.
- La lesividad de los implicados podría estar estadísticamente relacionada con el rango de edad.
- El tipo de accidente podría estar relacionado con el estado de ebriedad del conductor.
- La mayoría de los accidentes intraurbanos no requieren asistencia sanitaria, indicando que predominan los accidentes leves o sin lesiones visibles.
- Los puntos negros urbanos (tramos concretos de calles y autovías dentro de la ciudad) podrían concentrar un número desproporcionado de accidentes y deberían ser priorizados para medidas de prevención.

**Librerías**

Las librerías utilizadas han sido las siguientes: 

- Pandas
- Matplotlib 
- Numpy seaborn
- Unicodedata 
- Scipy.stats
- Geopandas
- Contextily
- Shapely
- Pyproj  
- Fiona

**Estructura del Repositorio**
Hay dos carpetas principales: Main y src. 

En Main se encuentran los notebooks limpios de los años 2020 a 2024 con los análisis completos que se llaman Main_EDA_Accidentalidad_"año correspondiente", y uno de general con comparaciones de todos los años que se llama Main_EDA_Accidentalidad.

En src se encuentran tres carpetas:

1. data: contiene los datasets descargados del [Ayuntamiento de Madrid](https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default)
y con los datasets limpios y procesados.
2. img: contiene las imágenes utilizadas en la memoria.
3. notebooks: notebooks en sucio del análisis

Además hay una memoria redactando el análisis, una presentación basada en este informe y un documento.

**Instrucciones de reproduccion**

Como tenemos 5 notebooks diferentes uno por cada año y el comparativo de todos los años, si quieres ver un año en concreto por ejemplo 2024 que es sobre el que se basa la memoria y la presentacion debemos abrir ese notebooks e ir ejecutando celda a celda de arriba a abajo. Arriba del todo en la primera celda estan importadas las librerias que se utilizan y luego ya seria ir ejecuntado por orden hacia abajo y de esta manera no tendrias ningun problema en la ejecución del código. Esto ocurriria con cualquiera de los notebooks de la carpeta Main que se quisiera utilizar.

**Principales conlcusiones**

Tras el análisis exploratorio, se contrastan las hipótesis planteadas al inicio con los resultados obtenidos:

- En el análisis temporal, se concluye que los meses con mayor número de accidentes fueron octubre, noviembre y diciembre, y no enero como se había planteado. En cuanto al día de la semana, aunque los lunes presentan una frecuencia relevante, son los viernes los que presentan la mayor proporción de accidentes. Asimismo, la franja horaria de mayor siniestralidad corresponde a la tarde (12:00-18:00), siendo las 18:00 la hora punta.  Por tanto, la hipótesis inicial no queda respaldada. 

- En el análisis geográfico, los datos muestran que los tres distritos con mayor número de accidentes fueron periféricos. No obstante, algunos de los céntricos también presentan una proporción elevada de accidentes. También se han identificado tramos concretos de las autovías A-2, A-42 y M-23 con concentraciones significativas de accidentes. Como conclusión, las hipótesis se confirman parcialmente.

- En relación al análisis demográfico, se observa que los jóvenes acumulan un número elevado de accidentes, especialmente en el rango de 25 a 29 años, sin embargo, el grupo con mayor número de accidentes corresponde al rango de 45 a 49 años. Por otro lado, la hipótesis de que los hombres presentan mayor frecuencia de accidentes que las mujeres, y que la mayoría de los implicados en los siniestros son conductores, queda respaldada por los datos. 

- En cuanto al análisis de los factores que influyen en un accidente, se observa que el turismo es el tipo de vehículo más frecuente. Por otra parte, aunque la colisión lateral presenta un número elevado de casos, el tipo de accidente más frecuente es la colisión fronto-lateral. Además, se respalda la hipótesis de que el estado de ebriedad del conductor está relacionado con el tipo de accidente, mediante el test Chi-cuadrado.

- Sobre la gravedad del accidente, predominan los accidentes leves o sin lesiones visibles, lo que confirma la hipótesis de partida. Además, el test Chi-cuadrado confirma que está estadísticamente relacionado con el rango de edad.
Adicionalmente al contraste de las hipótesis planteadas, los resultados del análisis indican que la distribución de los tipos de accidente no es homogénea entre los distintos distritos. También se observa que entre los distritos con mayor densidad de accidentes por km2, se encuentran algunos de los céntricos como Salamanca, Centro, Chamartín, Chamberí y Tetuán. Por otro lado, se confirma que la ebriedad del conductor está influenciada por la franja horaria y por la edad, de acuerdo con los resultados del test Chi-cuadrado. Además, que el grado de lesividad de los implicados está estadísticamente relacionado con el tipo de accidente, y que su distribución varía según el tipo de persona (conductor, pasajero o peatón), en función del sexo y la edad de las personas implicadas, y en función del distrito y del tipo de accidente.

- En conclusión, los resultados evidencian que la accidentalidad intraurbana en la ciudad de Madrid presenta patrones temporales, geográficos y demográficos relevantes, así como relaciones significativas con la lesividad y el contexto del accidente.


Además hay una memoria redactando el análisis, una presentación basada en este informe y un documento. 

**Autores**
- César Sánchez Parra
- Lucía Fuentes González
- Adrian Quindimil Rengel