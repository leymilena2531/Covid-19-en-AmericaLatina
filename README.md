**Expansión Estratégica de Biogenesys**


![logo_Biogenesys](https://github.com/leymilena2531/Covid-19-en-AmericaLatina/assets/114260905/379bce8d-1afb-4f3b-8f17-f444caa0b948)


# Introducción 👩‍💻

La empresa farmacéutica BIOGÉNESYS busca identificar las ubicaciones óptimas para la expansión de laboratorios farmacéuticos, basándose en el análisis de datos de incidencia de COVID-19, tasas de vacunación, y la disponibilidad de infraestructuras sanitarias. La meta es optimizar la respuesta a los efectos de la pandemia y post pandemia con el fin de mejorar el acceso a las vacunas.


# Desarrollo del proyecto 


# Avance 1 

Se aborda la carga, transformación y limpieza de datos para la expansión estratégica de Biogenesys en Latinoamérica.

# 1. Resumen del Avance
En este avance, se han realizado las siguientes tareas:
Lectura del archivo Readme.txt: Se analizó el archivo para comprender la descripción de las columnas del dataset.
Creación del notebook y carga de librerías: Se creó un notebook llamado "PIDA_M4_Nombre_Apellido.ipynb" y se cargaron las librerías Pandas, Numpy y Matplotlib.
Lectura del archivo data_latinoamerica.csv: Se leyó el archivo CSV utilizando Pandas.
Verificación de registros y columnas: Se verificó la cantidad de registros y columnas del dataset cargado.
Selección de países: Se seleccionaron los países de interés: Colombia, Argentina, Chile, México, Perú y Brasil.
Filtrado por fecha: Se filtraron los datos para fechas posteriores al 1 de enero de 2021.
Comparación por país para llenar valores faltantes: Se compararon los datos a nivel de país para llenar valores faltantes.
Limpieza preliminar de datos: Se eliminaron registros nulos y se corrigieron los tipos de datos.
Examen de características básicas: Se examinaron las características básicas del dataset.
Guardado de datos filtrados: Se guardaron los datos filtrados en un archivo CSV para su reutilización.
Cálculo de estadísticas descriptivas: Se calcularon estadísticas descriptivas para cada columna del dataset.

#2. Análisis de las Métricas

*Implicaciones*: Las métricas calculadas proporcionan información valiosa sobre la distribución y el comportamiento de las variables del dataset. Permiten comprender la centralidad, variabilidad, dispersión y forma de la distribución de datos, aspectos cruciales para el análisis posterior.

*Visualización de estadísticas*: Pandas solo muestra las estadísticas relevantes para el tipo de dato de cada columna.

*Datos numéricos*: Para datos numéricos, Pandas muestra medidas como media, mediana, moda, desviación estándar, mínimo y máximo.

*Datos categóricos*: Para datos categóricos, Pandas muestra la frecuencia de cada categoría.

 ## Conclusión
 
En este primer avance, se ha realizado la carga, transformación y limpieza inicial de los datos para la expansión estratégica de Biogenesys en Latinoamérica. 

## Análisis de las medidas 📉

*¿Qué representa la mediana?*

La mediana representa el valor central de un conjunto de datos ordenado. En otras palabras, si ordenamos los datos de menor a mayor, la mediana es el valor que se encuentra en la posición central (o el promedio de los dos valores centrales si hay un número par de datos).

*¿Cómo varía la dispersión de los datos en el conjunto de datos analizado, en términos de la varianza y el rango?*

**Varianza**: La varianza mide la dispersión promedio de los datos alrededor de la media. Una varianza alta indica que los datos están más dispersos, mientras que una varianza baja indica que los datos están más agrupados alrededor de la media.

**Rango**: El rango es la diferencia entre el valor máximo y el valor mínimo del conjunto de datos. Un rango alto indica que los datos están más dispersos, mientras que un rango bajo indica que los datos están más concentrados en un rango de valores más pequeño.

*¿Qué nos puede indicar esto sobre la consistencia o la variabilidad de los datos en relación con la mediana?*

**Varianza y mediana**: Si la varianza es alta y la mediana está cerca del valor mínimo o máximo, esto puede indicar que hay una gran cantidad de valores atípicos o valores extremos que alejan la media del valor central.

**Rango y mediana**: Si el rango es alto y la mediana está cerca del valor mínimo o máximo, esto puede indicar que hay una gran diferencia entre los valores más bajos y los valores más altos del conjunto de datos.

En resumen, la mediana, la varianza y el rango proporcionan información complementaria sobre la distribución de los datos. La mediana nos da una idea del valor central, mientras que la varianza y el rango nos indican cómo se dispersan los datos alrededor de la media. Al analizar estas medidas juntas, podemos obtener una mejor comprensión de la consistencia o la variabilidad de los datos.

## EXTRA CREDIT

*Explorando el uso de funciones de orden superior para la manipulación eficiente de datos*

Las funciones de orden superior son una herramienta poderosa en Python que permite procesar datos de manera más eficiente y flexible. Estas funciones pueden recibir otras funciones como argumentos y devolver nuevas funciones. 




**Definición de la función calcular_tasa_incidencia(casos, poblacion)**: 

-Esta función toma dos parámetros: un array casos que contiene la cantidad de casos confirmados de COVID-19 y un entero poblacion que representa la población total del país. 
-La función calcula la tasa de incidencia mensual dividiendo el número de casos por la población total y por 12 (para obtener la tasa mensual). 
-Luego, retorna la media de la tasa mensual.

**Agrupación de datos por país:** 

-El DataFrame df_latinoAmerica_paises_fecha se agrupa por el nombre del país utilizando el método groupby("country_name").

-Se seleccionan las columnas new_confirmed y population del DataFrame agrupado para ser utilizadas en la función apply().

**Cálculo de la tasa de incidencia para cada país**: 
-Se aplica la función calcular_tasa_incidencia() a cada grupo del DataFrame agrupado. 
-Esto se hace utilizando una función lambda que pasa las columnas new_confirmed y population a calcular_tasa_incidencia().

**sualización de los resultados**: 
-Se crea un gráfico de barras de las tasas de incidencia calculadas para cada país. 
-Se utiliza una lista de colores para las barras y se establecen los títulos de los ejes y del gráfico.

En resumen, esta función te permite calcular y visualizar la tasa de incidencia promedio mensual de COVID-19 por cada 100,000 habitantes para cada país en tu conjunto de datos. Esto puede ser útil para entender cómo la pandemia está afectando a diferentes países en términos relativos a su población.

**Beneficios de utilizar funciones de orden superior**:

-*Código más conciso y legible*: Las funciones de orden superior permiten escribir código más corto y fácil de entender, ya que se evita la repetición de código similar para diferentes casos.
-*Mayor flexibilidad*: Se pueden crear funciones más genéricas que pueden ser reutilizadas en diferentes tareas de análisis de datos.
-*Procesamiento de datos eficiente*: Las funciones de orden superior permiten procesar grandes conjuntos de datos de manera eficiente, ya que se pueden aplicar funciones a grupos de datos o a toda la estructura de datos en una sola línea de código.

**Ejemplos adicionales de uso de funciones de orden superior:**

*Filtrar datos*: Utilizar la función filter para seleccionar subconjuntos de datos que cumplan con una condición específica.
*Ordenar datos*: Utilizar la función sort para ordenar los datos según un criterio determinado.
*Transformar datos*: Utilizar la función apply para aplicar una función a cada elemento de una estructura de datos.
*Combinar datos*: Utilizar la función merge para combinar dos o más conjuntos de datos.

## Conclusión:
Las funciones de orden superior son una herramienta esencial para el análisis de datos en Python. Permiten escribir código más conciso, flexible y eficiente, lo que facilita la manipulación y el análisis de grandes conjuntos de datos. Al dominar el uso de estas funciones, los analistas de datos pueden obtener insights más valiosos de los datos y tomar mejores decisiones.

## Avance 2

**Análisis Exploratorio y Visualización de Datos**

Se centra en el análisis exploratorio y la visualización de datos relacionados con la incidencia de COVID-19, las tasas de vacunación y la disponibilidad de infraestructura sanitaria en diferentes países. El objetivo principal es identificar patrones, tendencias y anomalías en los datos para apoyar la toma de decisiones informadas sobre la ubicación de nuevos laboratorios y centros de vacunación.


## Importación de librerías:

Se importan las siguientes librerías para realizar el análisis y la visualización de datos:
pandas (para manipulación de datos)
numpy (para operaciones matemáticas)
matplotlib (para creación de gráficos)
seaborn (para visualización estadística)
datetime (para manejo de fechas)
Análisis Estadístico con Pandas y Numpy:
Se realizan las siguientes medidas de análisis estadístico para comprender mejor las características de los datos:
Medidas de tendencia central: Media, mediana y moda para variables numéricas.
Medidas de dispersión: Rango, varianza y desviación estándar para variables numéricas.
Correlaciones entre variables: Matriz de correlación y coeficientes de correlación de Pearson para identificar relaciones entre variables.


## Visualización de Datos con Matplotlib y Seaborn:

Se crean diversas visualizaciones para explorar los datos de manera gráfica:
Histogramas de densidad: Para observar la distribución de variables como casos confirmados y tasas de vacunación.
Gráficos de barras: Para comparar variables entre diferentes países o regiones.
Mapas de calor: Para identificar correlaciones entre variables.
Gráficos de dispersión: Para explorar posibles relaciones entre variables como temperatura media y casos confirmados/muertes confirmadas.



## Avance 3

**Informe del Avance 3: EDA con Numpy y Pandas**

*Introducción:*

En este avance 3 del proyecto, se realizó un análisis exploratorio detallado de los datos relacionados con la incidencia de COVID-19, utilizando técnicas avanzadas de Pandas y Numpy. El objetivo principal fue pulir y preparar los datos para una visualización avanzada que permita identificar con precisión las ubicaciones más estratégicas para la expansión de los laboratorios farmacéuticos.

**Metodología:**

**Carga y preprocesamiento de datos:**

-Se cargó el conjunto de datos utilizando pandas.
-Se inspeccionó la estructura del conjunto de datos.
-Se trataron los valores faltantes (imputación con la mediana).
-Se convirtieron las fechas a formato de fecha.

**Análisis de series temporales**:

**Tendencias:**

-Se analizó la evolución de casos activos vs. recuperados.
-Se calculó la tasa de crecimiento mensual de casos confirmados.
-Se graficaron las tendencias identificadas.

**Resultados:**

-Se identificaron tendencias generales en la evolución de casos activos, recuperados y confirmados.
-Se observó una estacionalidad en la serie de casos confirmados, con picos en algunos meses específicos.
-Se detectó autocorrelación en la serie de casos confirmados, lo que indica que los valores de la serie dependen de valores pasados.

Los resultados del análisis exploratorio proporcionan información valiosa sobre la evolución de la pandemia de COVID-19. La identificación de tendencias, estacionalidad y autocorrelación en las series temporales de casos permite comprender mejor la dinámica de la enfermedad y realizar pronósticos más precisos. La descomposición de series temporales también es útil para aislar los diferentes componentes que contribuyen a la variabilidad de la serie, lo que puede facilitar la identificación de factores que influyen en la propagación del virus.

**Conclusiones:**
El análisis exploratorio detallado realizado en este avance proporciona una base sólida para la visualización avanzada y el modelado de datos relacionados con la pandemia de COVID-19. La información obtenida a partir de este análisis puede ser utilizada para tomar decisiones informadas sobre la expansión de los laboratorios farmacéuticos y la implementación de estrategias de salud pública efectivas.

**Recomendaciones:**
Se recomienda continuar con el análisis avanzado de los datos, incluyendo la visualización interactiva y el modelado estadístico. Los resultados de estos análisis pueden ser utilizados para identificar patrones espaciales y temporales en la incidencia de COVID-19, así como para predecir la evolución de la enfermedad en diferentes regiones y países.

**Limitaciones:**
Es importante tener en cuenta que los resultados del análisis exploratorio están sujetos a las limitaciones de los datos disponibles. La calidad y la completitud de los datos pueden afectar la precisión de los análisis realizados.


## Avance 4

*Aplicaciones Prácticas - Integración en Power BI*

**Introducción:**

En este avance final del proyecto, se enfocará en la integración y presentación de los hallazgos analíticos y la elaboración de reportes utilizando Power BI para la visualización. El objetivo principal es sintetizar el análisis realizado en las fases anteriores en dashboards interactivos y reportes que faciliten la toma de decisiones estratégicas para la expansión de laboratorios y centros de vacunación.

**Metodología:**

*Conexión de Python con Power BI:*

-Se importará el conjunto de datos preparado y analizado en Power BI (archivo: "DatosFinalesParaPowerBI.csv").
-Se cargará el conjunto de datos en una tabla de Power BI.
-Creación de Dashboards en Power BI:
-Se diseñará un dashboard que muestre de manera efectiva los resultados del análisis de datos.
-Se utilizarán diferentes tipos de visualizaciones interactivas, como mapas, gráficos de barras, gráficos de líneas y gráficos de dispersión.
-Las visualizaciones permitirán a los usuarios explorar los datos de incidencia de COVID-19, cobertura de vacunación y variables relacionadas.
-Se utilizarán filtros y segmentaciones para permitir a los usuarios enfocarse en áreas específicas de interés.

*Visualizaciones Estáticas vs. Interactivas:*

-Se comparan los beneficios de utilizar gráficas estáticas para reportes impresos con las ventajas de las visualizaciones interactivas en dashboards digitales.
-Se destacó la capacidad de las visualizaciones interactivas para:
-Permitir la exploración de datos en profundidad.
- Facilitar la identificación de patrones y tendencias.
-Proporcionar una experiencia de usuario más atractiva e interactiva.
-Se crea un dashboard interactivo que muestra de manera efectiva los resultados del análisis de datos
-La integración de los resultados del análisis en Power BI permitirá a la empresa farmacéutica tomar decisiones estratégicas más informadas sobre la expansión de laboratorios y centros 
 de vacunación.
-Las visualizaciones interactivas y los dashboards facilitarán la comprensión de los datos y la identificación de áreas prioritarias para la inversión.

**Conclusiones:**
La utilización de Power BI para la visualización y presentación de datos es una herramienta valiosa para la toma de decisiones estratégicas. Las visualizaciones interactivas y los dashboards permiten explorar los datos en profundidad, identificar patrones y tendencias, y comunicar los resultados de manera efectiva a los stakeholders.

**Recomendaciones:**
Se recomienda continuar utilizando Power BI para explorar y analizar los datos de manera continua. Se pueden crear nuevos dashboards y reportes para monitorear el impacto de la pandemia de COVID-19 y evaluar la efectividad de las estrategias de vacunación.

**Limitaciones:**
Es importante tener en cuenta que la calidad y la completitud de los datos pueden afectar la precisión de los análisis realizados en Power BI.

**Agradecimientos:**
Agradecemos a Microsoft por el desarrollo de Power BI, una herramienta valiosa para la visualización y presentación de datos.
agradecemos a la empresa BIOGENESYS por su confianza y darnos la oportunidad de iniciar la carrera de Analistas de Datos con este proyecto

## Conclusiones Generales del Proyecto

A lo largo de este proyecto, se ha realizado un análisis exhaustivo de los datos relacionados con la incidencia de COVID-19 y las tasas de vacunación. El objetivo principal del proyecto era identificar tendencias, patrones y áreas prioritarias para la expansión de laboratorios y centros de vacunación por parte de una empresa farmacéutica.

**Principales hallazgos:**

*Tendencias:*
-Se han identificado tendencias generales en la evolución de casos confirmados, muertes, recuperados y tasas de vacunación a nivel global y por país.
-Se ha observado una estacionalidad en la incidencia de COVID-19, con picos en algunos meses específicos.
-Se ha detectado una relación entre la temperatura y la incidencia de COVID-19, con mayor número de casos en climas fríos.

*Patrones:*
-Se han identificado patrones geográficos en la distribución de casos confirmados, muertes y tasas de vacunación.
-Se han observado brechas en las tasas de vacunación entre países, regiones y grupos socioeconómicos.
-Se ha identificado una correlación entre la cobertura de vacunación y la reducción de casos y muertes por COVID-19.

*Áreas prioritarias:*
-Se han identificado las áreas con mayor incidencia de COVID-19, menor cobertura de vacunación o mayor vulnerabilidad como las áreas prioritarias para la expansión de laboratorios y 
 centros de vacunación.
-Se han considerado factores como la densidad poblacional, el acceso a la atención médica y los indicadores socioeconómicos para determinar las áreas prioritarias.

## Recomendaciones:

*Expansión estratégica*: La empresa farmacéutica debe enfocarse en expandir sus operaciones en las áreas prioritarias identificadas, donde existe una mayor necesidad de pruebas de diagnóstico, vacunas y tratamientos para COVID-19.

*Inversión en infraestructura:* Se recomienda invertir en la construcción de nuevos laboratorios y centros de vacunación en las áreas prioritarias, asegurando que se cuente con la 
 infraestructura y los recursos necesarios para satisfacer la demanda.
 
*Desarrollo de estrategias de vacunación personalizadas:* Se deben desarrollar estrategias de vacunación personalizadas para cada región y grupo socioeconómico, considerando las 
 características específicas de cada población.
 
*Monitoreo continuo*: Es importante monitorear continuamente la evolución de la pandemia de COVID-19 y las tasas de vacunación para adaptar las estrategias de expansión e inversión 
 según sea necesario.
 
## Impacto del proyecto:

Este proyecto ha proporcionado a la empresa farmacéutica información valiosa para tomar decisiones estratégicas sobre la expansión de sus operaciones en el contexto de la pandemia de COVID-19. Los resultados del análisis han permitido identificar áreas prioritarias para la inversión y desarrollar estrategias de vacunación más efectivas.

## Consideraciones adicionales:

Es importante tener en cuenta que la pandemia de COVID-19 es un fenómeno complejo y en constante evolución. La información y las recomendaciones presentadas en este proyecto deben ser revisadas y actualizadas periódicamente para adaptarse a los cambios en la situación epidemiológica.
La toma de decisiones estratégicas debe considerar no solo los aspectos epidemiológicos, sino también factores económicos, sociales y políticos.

## Conclusión:
 
Este proyecto ha demostrado la importancia del análisis de datos para la toma de decisiones informadas en el contexto de la pandemia de COVID-19. La integración de datos de diferentes fuentes, el uso de técnicas de análisis estadístico y la visualización interactiva de resultados han permitido obtener una comprensión profunda de la situación y formular recomendaciones estratégicas para la expansión de laboratorios y centros de vacunación.


**Análisis del dashboard**
- Página de inicio:
Ofrece una vista resumida del contenido del tablero . Desde cuál podrá acceder directamente a la información de cada una de las secciones. Así como, a una especial comparativa de datos.
- En cada sección: Contagios, decesos vacunados y recuperados.
Podrá apreciar las distribuciones de totales por localización y el ritmo de crecimiento, a lo largo del tiempo. Podrá seleccionar información concreta gracias a las segmentaciones, para mostrar las cantidades promedio.
- Resumen comparativo.
El informe identifica los países más afectados, en función de los datos acumulados y la relación entre contagios, vacunas y muertes. Las segmentaciones proporcionan información más significativa identificando lo ocurrido en países de Latinoamérica

**Conclusión:**
Este informe de Power BI sobre el análisis de la pandemia COVID19, ofrece información valiosa sobre la expansión del virus a lo largo del planeta, que se relaciona estrechamente con los recursos y cantidad de población, existente en cada país y planeta. Este análisis sirve como una poderosa herramienta para que los profesionales e investigadores tomen decisiones informadas, y se propongan protocolos y soluciones para estar mucho más preparados si esta situación u otra parecida, se diera de nuevo. 

## Conclusiones y Recomendaciones
La recomendación principal es una mejor recolección de los datos por que los datos eran en algunos casos nulos completamente lo que nos dejaba muy difícil el análisis
 



