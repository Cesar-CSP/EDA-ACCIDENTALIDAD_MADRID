# Introducción
Desde el año 2010, la Policía Municipal de Madrid ha registrado información detallada sobre todas las personas implicadas en los accidentes intraurbanos de la ciudad. 
En este proyecto se presentan las hipótesis de partida, el análisis exploratorio de los datos y las conclusiones derivadas de los datasets correspondientes
a los últimos cinco años, proporcionando una visión integral de los factores asociados a la siniestralidad y su evolución temporal, geográfica y demográfica.
El objetivo general de este EDA es determinar qué variables influyen de manera más significativa en la siniestralidad y la lesividad de los accidentes intraurbanos
en la ciudad de Madrid, así como analizar la relación entre ambas, con el fin de aportar evidencia que permita reducir la accidentalidad y mejorar la seguridad vial urbana. Los objetivos específicos son: 
1. Analizar los accidentes en Madrid desde una perspectiva temporal, geográfica y demográfica, evaluando la influencia de factores asociados y su relación con la lesividad, para identificar periodos, zonas y condiciones de mayor riesgo.
2.	Establecer posibles relaciones bivariantes y multivariantes entre variables, para identificar patrones y asociaciones relevantes para la seguridad vial.
3.	Proporcionar recomendaciones basadas en los resultados, priorizando intervenciones en los periodos, zonas y situaciones de mayor riesgo.

**Librerías**

Las librerías utilizadas han sido las siguientes: datetime, pandas, matplotlib, numpy seaborn, unicodedata, scipy.stats, geopandas y contextily.

**Estructura del Repositorio**
Hay dos carpetas principales: Main y src. En Main se encuentran los notebooks limpios de los años 2020 a 2024 con los análisis completos, y uno de general con comparaciones de todos los años.
En src se encuentran tres carpetas:
1. data: contiene los datasets descargados del [Ayuntamiento de Madrid](https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default)
y con los datasets limpios y procesados.
2. img: contiene las imágenes utilizadas en la memoria.
3. notebooks: notebooks en sucio del análisis

Además hay una memoria redactando el análisis, una presentación basada en este informe y un documento 
