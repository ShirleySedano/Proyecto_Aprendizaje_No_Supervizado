## Primera entrega: Análisis y agrupación de quejas realizadas por usuarios de una aerolínea a través del análisis de sentimientos.

### Integrantes:

Andrés Parra Garzón

Carlos Cañas Díaz

Shirley Sánchez Sedano

### Resumen:

El análisis, priorización y solución oportuna de quejas de los clientes es una tarea importante en la prestación de un servicio, y más aún en un sector como el de aerolíneas, donde cada día la competencia en precios es más agresiva; es ahí donde la velocidad de solución de problemas inherentes a la operación cobra importancia para maximizar la satisfacción del cliente. El presente proyecto busca, haciendo uso de las quejas puestas por los clientes de una aerolínea a través de diferentes medios de contacto, generar segmentación de estas, que permita conocer el nivel de insatisfacción y el sentimiento que tuvo el cliente al escribirla. Esto permitirá clasificar las quejas en las cuales el cliente está inconforme pero calmado y su solución puede esperar un tiempo prudente , hasta las quejas donde el cliente se encuentra muy molesto y necesita atención inmediata para su problema, asociado al proceso donde se presenta la queja: no es lo mismo un cliente que después de su vuelo tuvo un problema con equipaje dañado, el cual puede estar molesto pero se puede solucionar en cierto tiempo, que un cliente que se encuentra haciendo check-in en el aeropuerto y su reserva no aparece, el cual necesita atención inmediata y su nivel de inconformidad es mayor. 

La complejidad de esta tarea reside en dos pasos importantes: el primero es ser capaces de utilizar una queja escrita por una persona, la cual es una línea de texto o un párrafo sin estructura, y convertirla en información que sea utilizable y comparable con otras quejas recibidas. Para esto, haciendo uso de técnicas de procesamiento del lenguaje natural y de análisis de sentimientos, se transformarán estas quejas de manera que tengan información útil del contenido de la queja, el sentimiento del cliente cuando la escribió y el nivel de inconformidad que tuvo al escribirla. El segundo paso importante es, con esta información transformada, cómo poder agrupar miles de quejas recibidas en grupos homogéneos que permita darle a la empresa información valiosa de cuáles son las más urgentes por atender y resolver, y cuáles pueden ser resueltas más adelante. Para esto se utilizarán técnicas de segmentación de datos, las cuales buscan patrones internos en la información y que tan parecidas son las quejas, independientemente de las palabras usadas, el largo del texto de la queja y del lenguaje utilizado por la persona. Si se contaran con pocas quejas esto sería una tarea sencilla para una persona, pero al contar con miles de quejas por día, se hace necesario hacer uso de técnicas más avanzadas. 

### Introducción:

Propuesta: Análisis y agrupación de quejas realizadas por usuarios de una aerolínea a través del análisis de sentimientos. 

La satisfacción de los clientes es el indicador directo de crecimiento tanto en ingresos como en imagen de una organización. Por lo tanto, no dar solución adecuada a las reclamaciones de los usuarios puede afectar de manera importante la reputación de la entidad, generando pérdida de clientes y dinero. Por lo que, el propósito de este proyecto es realizar agrupación de las quejas realizadas a una aerolínea para posteriormente hallar diferentes grados de severidad de esta, con el propósito de identificar cuáles son las quejas más recurrentes, cuales se deben resolver con mayor prontitud y además aprovechar las inconformidades para implementar medidas que ayuden a mejorar los procesos de la aerolínea. 

La solución de este problema es de gran importancia para la aerolínea que recibe las quejas, sobre todo para las áreas relacionadas con la solución de estas como el área de marketing, servicio al cliente y gestión de PQRS. 

### Revisión preliminar de la literatura:

#### 1.Detección de sugerencias en tuits de usuarios y seguidores de aerolíneas con minería de sugerencias: 

Este trabajo de grado se centra en la recolección de tuits creados por usuarios de aerolíneas mexicanas: Aeroméxico, Interjet, TAR, Viva Aerobús y Volaris. En total se recolectaron 21.161 comentarios que se escribieron entre el 9 de agosto y el 27 de octubre del 2019. 

El análisis consiste inicialmente en realizar procesamiento de lenguaje natural donde se pasan todos los comentarios a minúsculas, se eliminan acentos, emoticones, comillas, guiones bajos, stopwords y caracteres numéricos. Este procedimiento es similar al realizado en nuestro proyecto, además de que trata del mismo tema. Sin embargo, en esta tesis se hace uso de personas externas para etiquetar los comentarios según una clasificación de sugerencias, y hacer uso finalmente modelos supervisados, este es nuestra gran diferencia ya que nuestro problema es de carácter no supervisado. 

#### 2. Identificación y análisis de quejas en Twitter de los principales bancos en México de 2018 a 2019 mediante técnicas de minería de datos y recuperación de información: 

En esta tesis como dice su título, se centra en las quejas que se les realizan a los principales bancos en México. Con el fin de buscar tendencias y detectar comportamientos similares, el procedimiento en este caso consistió en realizar el procesamiento de lenguaje natural donde después de cambiar el texto a minúsculas, eliminar acentos, caracteres especiales, URL, signos de puntuación y stopwords, usar unigramas y ponderación con TF-IDF; se realiza el proceso de clusterización por medio de K-medias en donde se pueden identificar los temas correspondientes a cada grupo de queja, posteriormente a cada clúster se crea una subdivisión por medio de clustering jerárquico divisivo con el criterio Ward. Aunque el tema no es similar, este trabajo nos da ideas para que una vez empleemos NLP no quedarnos únicamente con la clusterización inicial, sino analizar cada grupo con el objetivo de realizar subdivisiones dentro de cada agrupación de quejas. 

#### 3. Humanizing Customer Complaints with NLP Algorithms: 

En este artículo se muestra la importancia de prestar atención a las emociones humanas en cada una de las quejas para realizar un mejor análisis, y es por esto que en uno de los casos del artículo se presenta el “análisis de sentimientos”. Inicialmente se realiza el procesamiento de lenguaje natural, el cual es explicado de manera teórica el detalle de los pasos a seguir, para posteriormente realizar la agregación del sentimiento asociado a cada queja y realizar las respectivas agrupaciones de esta. Este artículo es de interés en nuestro proyecto, ya que nos muestra la importancia de realizar el análisis de sentimientos para obtener mejores resultados. 

#### 4. Using Text Mining and Cluster Analysis to Improve Customers Complaints System: 

En este trabajo el objetivo es utilizar métodos de minería de texto y agrupamiento para mejorar el sistema de quejas de los clientes de un sistema de transporte. Para realizar la minería de texto se utilizó el software Rapid Miner y posteriormente se realizó clusterización con K-medias. Aunque la temática del trabajo no es igual ni el procesamiento inicial de las quejas, ya que en nuestro caso se realizará procesamiento de lenguaje natural, la finalidad es la misma al realizar el agrupamiento por medio de técnicas de aprendizaje no supervisado. 

### Descripción de los datos:

Antes de iniciar la descripción de los datos es importante aclarar que no se subirán en este repositorio los datos originales por cuestiones de confidencialidad

A continuación se presenta una sintesis del procesamiento de lenguaje natural realizado y sus estadísticas descriptivas. Los detalles se pueden encontrar en el siguiente [link](https://github.com/ShirleySedano/Proyecto_Aprendizaje_No_Supervizado/blob/main/An%C3%A1lisis%20descriptivo%20y%20NLP)

#### Cantidad de palabras por mensaje

![Imagen 1. Cantidad de palabras por mensaje (sin preprocesamiento](https://user-images.githubusercontent.com/102918996/188344129-48c5ae60-9e64-48f6-8f83-793434555c38.png)

![Imagen 2. Cantidad de palabras por mensaje (con preprocesamiento)](https://user-images.githubusercontent.com/102918996/188343877-d82c4d0f-469f-4ef4-9be2-6e312d5fcc82.png)

En esta comparativa se observa que la mayoría de los mensajes conserva su densidad de palabras aún después del preprocesamiento, salvo para un pequeño grupo para el cual se reduce significativamente su cantidad de palabras a menos de mil. 

#### Palabras que más se repiten

![Imagen 3. Palabras que más se repiten en mensaje (sin preprocesamiento)](https://user-images.githubusercontent.com/102918996/188344426-ffc5b56e-97a7-4fc1-867d-4d9cfe2a6a0b.png)

![Imagen 4. Palabras que más se repiten en mensaje (con preprocesamiento)](https://user-images.githubusercontent.com/102918996/188344557-17c94d66-b199-4206-b91f-a908fb072a4f.png)

En esta comparativa hay varios aspectos relevantes a destacar: se observa el ruido que hacen los stopwords sobre la data, el incremento en la frecuencia de algunas palabras como resultado del proceso de lematización, y que hay mensajes en otros idiomas diferentes al español que habrá que manejar. 

#### Named Entity Recognition (NER)

![Imagen 5. Aplicación de NER (sin preprocesamiento) ](https://user-images.githubusercontent.com/102918996/188344704-9c7d5ea1-5037-4d05-b1aa-276e80811c57.png)

![Imagen 6. Aplicación de NER (con preprocesamiento) ](https://user-images.githubusercontent.com/102918996/188344784-7dd1cf27-f1af-4367-9e4d-5d14bcfd7316.png)

Al hacer el análisis de reconocimiento de entidades vemos que al principio prima la información geográfica por sobre el resto. Luego del preprocesamiento se logran identificar más personas. Asimismo, es destacable que la información miscelánea también crece.

#### Part of Speech (POS)

![Imagen 7. Aplicación de POS (sin preprocesamiento) ](https://user-images.githubusercontent.com/102918996/188344999-f29a0614-ba9b-4cc1-b1ab-06a55c5cd767.png)

![Imagen 8. Aplicación de POS (sin preprocesamiento) ](https://user-images.githubusercontent.com/102918996/188345096-46a8f797-a7b0-420c-bed8-6f4b63188c86.png)

En el análisis POS vemos que antes del preprocesamiento la información es bastante variada, gramaticalmente hablando; sin embargo, luego de procesar la base, la información se concentra en nombres, nombres propios, verbos y adjetivos. 

Adicional a los análisis anteriores, se realizaron otros que no se colocaron en el documento por restricciones de espacio. Se realizaron los análisis: cantidad de caracteres por mensaje, tamaño promedio de palabra, bigramas y trigramas que más se repiten

La matriz de quejas resultante despues de NLP es la [siguiente](https://github.com/ShirleySedano/Proyecto_Aprendizaje_No_Supervizado/blob/main/MATRIZ_QUEJAS_TFIDF.zip)

### Propuesta metodológica:

Para el componente de Procesamiento de lenguaje natural se hará uso de técnicas de limpieza de datos, eliminando palabras utilizadas normalmente por las personas, pero que no agregan significado a la queja, como lo son los conectores, nombres propios, número de identificación, entre otros. Luego de esta limpieza se realizará el proceso de tokenización de las quejas con diccionarios especializados disponibles en el idioma español, que permita agrupar palabras con raíces similares, o grupos de palabra que por sí solas no tienen significado, pero con el uso en conjunto con otra palabra sí, todo esto con el fin de reducir la cantidad de palabras que se convertirán en variables del modelo de clustering. 

Para el componente de clustering inicialmente se propone utilizar un modelo DBSCAN, el cual tiene la ventaja de no tener que clasificar necesariamente todos los componentes de la base de datos en un clúster, y que muestre al usuario posibles outliers y que potencialmente estos outliers sean los clientes con mayor urgencia e inconformidad de la información disponible. Como segundo posible algoritmo a utilizar se propone el modelo aglomerativo jerárquico, ya que las quejas están asociados a un proceso de la compañía. Este esquema permitirá ir agrupando quejas tanto por su nivel de incomodidad como por el proceso el cual está asociado, para así finalmente tener un único clúster.

#### Bibliografía. 

-Jiménez Castro, R. (2021). Detección de sugerencias en tuits de usuarios y seguidores de aerolíneas con minería de sugerencias. Instituto de Ingeniería y Tecnología.- 

-Armas, D. (2020). Identificación y análisis de quejas en Twitter de los principales bancos en México de 2018 a 2019 mediante técnicas de minería de datos y recuperación de información.  

-Morde, V., 2022. Humanizing Customer Complaints with NLP Algorithms. [online] Linkedin.com. Available at: <https://www.linkedin.com/pulse/humanizing-customer-complaints-nlp-algorithms-vishal-morde/> [Accessed 1 September 2022].  

-HASAN, S. (2018). Using Text Mining and Cluster Analysis to Improve Customers Complaints System (Doctoral dissertation, The British University in Dubai (BUiD)). 

Para descargar el PDF dar click en el siguiente [link](https://github.com/ShirleySedano/Proyecto_Aprendizaje_No_Supervizado/blob/main/PROPUESTA%20INICIAL_SEMANA%204_CALIFICABLE.pdf)

 
## Entrega final: Análisis y agrupación de quejas realizadas por usuarios de una aerolínea latinoamericana

### Resumen

El análisis, priorización y solución oportuna de quejas de clientes es una tarea importante en la prestación del servicio en el transporte aéreo, donde cada día surgen nuevas aerolíneas y por lo tanto la competencia es cada vez mayor; es ahí donde la velocidad de solución toma importancia para maximizar la satisfacción de los usuarios. 
El presente proyecto tiene como objetivo segmentar y analizar un conjunto de quejas interpuestas por clientes de una aerolínea latinoamericana a través de diferentes medios de contacto, con el propósito de conocer la naturaleza de los reclamos y el nivel de insatisfacción del cliente. Esto permitirá dar solución a los reclamos según su nivel de urgencia. Para lograr lo anterior, se hizo uso de técnicas de procesamiento de lenguaje natural con el fin de transformar los textos escritos por los usuarios en datos utilizables por el modelo de K-means dando como resultado seis agrupaciones. Según los resultados arrojados por cada clúster se puede evidenciar, en general, la temática de cada uno de ellos, sin embargo, para futuros análisis es importante probar nuevas técnicas de NLP para mejorar el proceso de limpieza y tener como resultado agrupaciones disjuntas entre sí.

### Introducción

La satisfacción de los clientes es el indicador directo de crecimiento tanto en ingresos como en imagen de una organización. Por lo tanto, no dar solución adecuada a las reclamaciones de los usuarios puede afectar de manera importante la reputación de la entidad, generando pérdida de clientes y dinero. Por lo que, el propósito de este proyecto es realizar agrupación de las quejas realizadas a una aerolínea latinoamericana para posteriormente hallar diferentes grados de severidad de esta, con el fin de identificar cuáles son las quejas más recurrentes, cuales se deben resolver con mayor prontitud y además aprovechar las inconformidades para implementar medidas que ayuden a mejorar los procesos de la aerolínea.

 La solución de este problema es de gran importancia para la aerolínea que recibe las quejas, sobre todo para las áreas relacionadas con la solución de estas como el área de marketing, servicio al cliente y gestión de PQRS.
 
En la literatura existe diversa información con respecto a este tema. Aldunate, Á (2022) en su artículo presenta la importancia de comprender los factores que influyen en la satisfacción del cliente a través del análisis de encuestas por medio del procesamiento de lenguaje natural y a partir de allí crear un modelo supervisado. Por su parte, Gavval, R., & Ravi, V. (2020) enuncia la necesidad de resolver oportunamente las reclamaciones para evitar pérdidas económicas, es por eso que en su artículo sobre agrupación de quejas de clientes bancarios por medio de redes sociales evidencia como el algoritmo de K-medias y variantes de este funcionan muy bien a la hora  de realizar las agrupaciones. 

### Materiales y Métodos.

#### Datos utilizados:

La base de datos a utilizar es un lote de quejas históricas realizadas por clientes de una aerolínea latinoamericana, la cual fue preparada y compartida específicamente para este ejercicio académico. La información para explotar son los mensajes colectados que contienen el detalle de la queja o reclamo. La base cuenta con 10 mil observaciones.

#### Proceso de limpieza de los datos:

Para preparar la data a partir de los mensajes de texto, que nos permitirá construir las variables que van a alimentar nuestro modelo de aprendizaje no supervisado, se utilizaron las siguientes técnicas de Lenguaje de Procesamiento Natural (NLP): 1. Inferencia del idioma para tomar en cuenta sólo los mensajes en español, 2. Exclusión de palabras y patrones en el texto usando expresiones regulares, 3. Tokenización, 4. Eliminación de stopwords, 5. Lematización, 6. Exclusión de nombres propios usando Part of Speech (POS), por mencionar las más relevantes.

#### Estadísticas descriptivas de los datos:

Para realizar la exploración de los mensajes contenidos en la base de datos, se llevó a cabo la siguiente estrategia: 1. Lectura de datos crudos, 2. Cálculo de estadísticas de los mensajes sin y con preprocesamiento, 3. Comparativa de estadísticas y análisis de resultados. A continuación, se muestra un resumen de algunas de las estadísticas descriptivas calculadas sobre el texto:

![Tabla 1. Listado de estadísticas para ilustrar la diferencia entre los datos originales y los preprocesados](https://user-images.githubusercontent.com/102918996/192166766-478381b5-7ebd-40ea-b308-e6018464c89e.png)

#### Construcción de variables:

Para realizar la construcción de las variables a partir del texto preparado anteriormente, utilizamos la técnica llamada Term Frequency-Inverse Document Frequency (TF-IDF), la cual se caracteriza por darle importancia a las palabras que le dan significado al mensaje por sobre las que no. Primero se calcula la frecuencia del término en función del total de términos en el mensaje (Term Frequency) y luego se calcula el peso que permite identificar fácilmente los términos que no se repiten tanto o no son tan relevantes (Inverse Document Frequency).

### Algoritmo de clustering seleccionado:

El algoritmo de K-Medias forma parte de los algoritmos de clustering basados en centroides, el cual agrupa las observaciones en un número predefinido de K clústeres de forma que, la suma de las varianzas internas de los clústeres sea lo menor posible. Esto se logra en cada clúster a través de la suma de todos los pares de distancias euclidianas cuadráticas de las observaciones, dividida por el número total de observaciones en el mismo. Este proceso se repite hasta que las asignaciones llegan al punto en que no cambian.

Para aplicar el algoritmo K-Medias se utilizó la función KMeans de Sklearn, cuyos parámetros principales son los siguientes:

•	n_clusters: Número de clústeres predefinido

•	init: Método de inicialización para asignar los centroides iniciales, puede ser alejándolos lo más posible o asignándolos aleatoriamente

•	n_init: Número de veces que se va a repetir el proceso, cada vez con una asignación aleatoria inicial distinta

•	max_iter: Máximo de iteraciones permitidas

### Algoritmos utilizados:

Luego de realizar la transformación de los datos mediante el uso de TF-IDF se realizaron pruebas utilizando los siguientes algoritmos: K-medias, Jerárquico aglomerativo, DBSCAN y detección de comunidades. Analizando los resultados de cada uno de ellos obtenemos que:

•	Haciendo uso del algoritmo jerárquico aglomerativo se obtiene un clúster de mayor tamaño frente a los demás clústeres, y no se logran encontrar un diferenciador contundente entre los diferentes grupos. Al analizar las palabras dentro de los clústeres se encuentra que vuelo, maleta, esperar, compensación aparecen en cada uno de ellos, con diferente frecuencia. Se encontraron 5 clústeres usando esta técnica.

•	El algoritmo DBSCAN logró identificar algunos outliers de la información, sin embargo, la calibración del épsilon mediante las técnicas estudiadas no ayudó a este fin, por lo que mediante prueba y error se intentó identificar un valor, pero no fue posible, se obtuvo al igual que en al caso anterior un clúster más grande que los demás, sin ninguna diferenciación importante en cuanto frecuencia de los datos.

•	Con detección de comunidades se lograron encontrar 15 clústeres, con información satisfactoria que da noción de la temática de la queja y de la severidad de esta, sin embargo, la técnica no permite seleccionar la cantidad de grupos deseados, en cambio solo permite seleccionar la cantidad mínima de elementos para conformar un clúster, es por esto que algunos de los clústeres conformados fueron muy similares a otros, y el análisis de 15 clústeres se hizo complejo.

•	K-medias también logró resultados satisfactorios y relevantes, siendo capaz de clasificar la temática de la queja, el origen de estas y la severidad de acuerdo con las palabras únicas que presentaron alta frecuencia. Como fue posible seleccionar la cantidad de clústeres y los clústeres generados son parecidos a los de detección de comunidades en cuanto a las palabras únicas que dan sentido al grupo, se selecciona esta técnica como la adecuada para el problema de este proyecto
Resultados del algoritmo seleccionado.

Para el algoritmo de K-medias se hizo uso del coeficiente de Silhouette con el fin de encontrar la cantidad de clústeres adecuados. Los resultados se pueden observar a continuación:
 
![Gráfica 1. Coeficiente de Silhouette](https://user-images.githubusercontent.com/102918996/192167713-5687d776-579b-44fa-9104-a5978e5aaf7f.png)

Podemos observar que el valor del índice no es muy variable para los primeros 40 clústeres, teniendo un máximo en 35. Para la primera iteración se utiliza esta cantidad de clústeres y se analiza el resultado. Para el análisis de resultado se utilizará la técnica de reducción de dimensionalidad y visualización t-SNE propuesta por Van der Maaten y Hinton (2008), la cual se ajusta a problemas de alta dimensionalidad como es este caso, embebiendo los datos en un espacio de dos o tres dimensiones para su visualización, donde elementos con alta probabilidad de ser similares se modelan como puntos cercanos, y elementos con baja probabilidad de ser similares se modelan como puntos lejanos. 

Inicialmente utilizando esta técnica, sin ninguna etiqueta de clúster, los datos se visualizan como la gráfica 2. Se observa una nube de puntos muy homogénea, con algunos pequeños grupos focalizados en la periferia de la gráfica. 

Ahora bien, haciendo uso de K-medias con 35 clústeres, el resultado se muestra en la gráfica 3. El algoritmo fue capaz de agrupar y separar los pequeños grupos observados previamente, sin embargo, los clústeres se encuentran superpuestos unos con otros, esto afianza la suposición inicial de que la información suministrada es muy homogénea en cuanto a los elementos y palabras que contienen las quejas.

Debido a este resultado, y a la complejidad de análisis de 35 clústeres, se decide iterar mediante ensayo y error disminuyendo la cantidad de clústeres hasta encontrar una solución satisfactoria, que pueda clasificar la nube central, pero que nos permita identificar esos pequeños grupos de las periferias. Dicho número de clústeres propuesto es 6. Con 6 clústeres y volviendo a usar la técnica t-SNE, podemos ver el resultado final en la gráfica 4.

![image](https://user-images.githubusercontent.com/102918996/192167694-c54f1ec4-690e-4e41-8e38-fb17603f59e0.png) 	 	

A pesar de que se sigue presentando superposición de clústeres, los grupos se encuentran más definidos y los valores lejanos del clúster son menores, aunque presentes. Vemos como las periferias se encuentran clasificadas. Para entender que tipo de quejas se encuentran en cada clúster, se hace uso de nubes de palabras que permita visualizar las palabras con mayor frecuencia dentro del clúster:

![Gráfica 5. Comparativo de clústeres obtenidos a través de nubes de palabras](https://user-images.githubusercontent.com/102918996/192167672-f5aa9faf-130c-44b2-83aa-9a003adfaee4.png)

Vemos como existen palabras dominantes en cada clúster, sin embargo, en algunos de ellos no son palabras que permitan independizar el grupo de los demás, como es el caso del clúster 5 donde pasajero e indicar prevalecen. El clúster cero se caracteriza por las llamadas hechas por call center donde se crea el caso por daño en el equipaje, donde el cliente expresa ser compensado. El clúster 1 se caracteriza por inconformidad en las demoras y en los problemas operativos de las rutas. El clúster 2 lo conforman las quejas en el cual el cliente solicita información por equipaje perdido. El clúster 3 es en el que la palabra compensación prevalece, pero no es claro la temática de la queja, pero si el sentimiento de urgencia del cliente. El clúster 4 y el clúster 5 son los de mayor cantidad de elementos, donde maleta, equipaje, pasajero prevalecen, pero no es claro ni la temática ni el sentimiento. Los clústeres se pueden resumir en la siguiente tabla:

![Tabla 2. Resumen de clústeres obtenidos usando K-Medias (k=6)](https://user-images.githubusercontent.com/102918996/192167450-7a9a725e-6081-4f44-aa64-ce53cc5a85bc.png)

El análisis completo y detallado del paso a paso del análisis y sus resultados se pueden encontrar en el siguiente  [link](https://github.com/ShirleySedano/Proyecto_Aprendizaje_No_Supervizado/blob/main/CODIGO%20PROYECTO%20FINAL.ipynb)

### Conclusión:

Con respecto a este proyecto se puede concluir que los resultados dependen fundamentalmente de la calidad de las variables seleccionadas a ingresar al modelo, es por esta razón que gran parte del tiempo se implementó en realizar una correcta limpieza de los datos, la cual consistió principalmente en elegir únicamente las quejas en idioma español, eliminar caracteres especiales, espacios, URL, números, emojis y stopwords. Además, se eliminó de manera manual un conjunto de palabras vacías que no aportaban al análisis, estas de detectaron una vez se implementó TF-IFD.

Fue importante escoger un buen paquete en Python para realizar la lematización, ya que la mayoría de las funciones están hechas para realizar un buen análisis en el idioma inglés. Por lo anterior se eligió Stanza, un paquete creado por un grupo de la universidad de Stanford, donde su característica principal es que se trata de modelos neuronales pre-entrenados que admiten 70 idiomas, entre ellos el español.

Una vez ingresadas las variables al modelo de K-medias se obtienen 6 clúster donde 4 de ellos se pueden observar claramente su temática, sin embargo, se evidencia que estas segmentaciones se traslapan entre sí en cuanto a sus términos más frecuentes.
Se recomienda para análisis futuros implementar otras técnicas y lematizadores en el idioma español para lograr una mejor limpieza de los datos, y explorar otros algoritmos de aprendizaje no supervisado que por cuestiones de tiempo no se pudieron probar. Además, realizar análisis dentro de cada clúster, es decir, es nuestro caso de observa que aún las características para cada segmentación son muy generales, por lo tanto, sería interesante aplicar análisis no supervisado dentro de cada clúster.

### Bibliografía:

Aldunate, Á., Maldonado, S., Vairetti, C., & Armelini, G. (2022). Understanding customer satisfaction via deep learning and natural language processing. Expert Systems with Applications, 209, 118309.

Gavval, R., & Ravi, V. (2020). Clustering bank customer complaints on social media for analytical CRM via multi-objective particle swarm optimization. In Nature Inspired Computing for Data Science (pp. 213-239). Springer, Cham.

Van der Maaten, L., & Hinton, G. (2008). Visualizing data using t-SNE. Journal of machine learning research, 9(11).

Para descargar el PDF dar click en el siguiente [link](https://github.com/ShirleySedano/Proyecto_Aprendizaje_No_Supervizado/blob/main/SEMANA%207%20PROYECTO%20FINAL%20TERMINADO.pdf)
