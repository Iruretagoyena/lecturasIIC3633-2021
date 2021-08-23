# Semana 1

#### Tema: UBCF
#### Entrega: 23 de Agosto, 8pm
Lecturas leídas:
- [x] Collaborative Filtering Recommender Systems 
- [x] Item-based collaborative filtering recommendation algorithms. In Proceedings of the 10th international conference on World Wide Web
- [x] Post original FunkSVD
- [x] Slope One Predictors for Online Rating-Based Collaborative Filtering.

El resumen se basa en la lectura de Collaborative Filtering Recommender Systems, mencionando algunos detalles y comparaciones con las otras 3 lecturas (propuestas como opcionales).

## Resumen semana 1

#### Introducción y Abstract

El paper propuesto habla principalmente sobre **Collaborative Filtering** (Filtrado por Colaboración), el cual se entiende como el proceso de filtrar o evaluar ítems según la opinión de otras personas.

Se introducen los pilares fundamentales de adaptive web, la teoría y practica de los algoritmos usados en el Filtrado por Colaboración y las decisiones de diseño que entrañan los sistemas de ratings y adquisición de ratings. Se discute además cómo se evalúan esto sistemas y se habla de la evolución de interfaces de interacción. Se finaliza hablando sobre privacidad y preguntas abiertas en este campo.

#### Comentarios personales y criticas acerca de las lecturas

Me gustó harto el paper ya que siento es una buena introducción a los temas del curso.
Se plantea la historia y razón de ser del uso de opiniones para recomendar, mencionando que si bien el área tiene ~20 años, esto de dar nuestra opinión y juzgar en base a eso lo venimos haciendo desde siempre. Qué mejor para evaluar una cosa que algún conocid@ ya lo haya experimentado ?
Esto se traduce en muchas áreas de la vida y explica "comportamientos rebaño" en la sociedad hoy en día. Se explican métodos usados, aterrizamiento matematico de algunos conceptos y ventajas/problematicas de cada sistema.

Me gusta que se formalicen los conceptos desde un principio, como rating, usuario, rating implicito/explicito, etc. 

"In this way, collaborative filtering enables the web to adapt to each individual user’s needs."
Me gustó esta frase ya que alude a como los RecSys optimizan la web frente a su limitación de atención de usuario y de espacio en pantalla.

Me gustó lo del "meta-recommendation system" pero encontré que lo explican muy a la pasada, por lo que no me queda tan claro el sistema (aunque parece que ahondan en una sección no incluida en esta lectura). Me hubiese gustado una mayor explicación de esos sistemas, ya que se utilizan en un caso concreto.

Encontré interesante lo mencionado sobre las cualidades necesarias (o idoneas) para los RecSys (la parte de data distribution, underlying meaning, and data persistence), pero encontré que faltaban argumentos para fijar esos pilares. Hay aseveraciones muy tajantes sobre que si y que no, encuentro que faltan argumentos concretos (o quizás son obvias y es mi falta de dominio en el tema).

Se habla de algo muy importante en el tema de vecinos cercanos pero de forma muy superficial. "these skewed neighbors can dominate a user’s neighborhood" me gustó esa explicación pero siento que faltó más detalle (algún gráfico que evidencie esto) ya que es un detalle muy importante pero se dijo a la pasada.

En la explicación de los desafíos en los Item-Based Algs, se menciona "In practice, we can substantially reduce this size by only storing correlations for item pairs with more than k coratings", pero, qué K se elige ? Cómo saber que hiperparametro elegir ? Me hubiese gustado más detalle.

Encontré que la sección "Beyond Accuracy" era muy interesante pero se quedaba corta; cómo utilizo toda esa información ? Cuál priorizo ? Hay ejemplos concretos de usos de estas metricas ? Cómo las mezclo entre si, en especial si parto desde un cold start ?

Personalmente me interesa el tema de Privacidad y Seguridad, por lo que encontré que faltaba más información al final del paper sobre este tema. Qué medidas se toman actualmente ? Ejemplos de leyes vigentes ? Casos de multas a empresas ? Cómo enfrentar esto ?
Si bien se menciona, se podría haber detallado más. Creo que se ahonda más pero en secciones no incluidas en la lectura.
Se podrían haber mencionado más casos reales de los "shilling attacks"

En la conclusión se resumen algunas limitantes que creo ya han tenido grandes avances (cabe tener en cuentra que el paper es del 2007) en especial con el uso de Computer Vision para recomendar cosas según el "estilo", lo cual no es captado por las reviews o la escala numerica de una reseña. Sería interesante leer un paper de estos mismos autores en la actualidad, para que respondan ciertas inquietudes planteadas. 
Incluso en el area de privacidad ya han habido casos importantes.


#### Relación con lecturas opcionales

Creo que las otras 3 lecturas eran muy interesantes y tenian fuerte relación con el paper principal.
"Slope One Predictors" mencionaba claramente una opción frente a los esquemas basados en memoria obteniendo iguales/mejores resultados con menor información, detalle que se menciona en el paper principal, superando esa ineficiencia.

"FunkSVD" fue en lo personal mi favorito, ya que materializaba de forma muy concreta un ejemplo de uso de estas técnicas (SVD), en el contexto del "Netflix Price" mencionado en clases. No me quedaron tan claros los gráficos finales, pero me gustó mucho que fuese un formato "más libre" que el de un paper, ya que permite otra forma de narrar la historia.

"Item-Based Collaborative Filtering Recommendation Algorithms" era bien interesante ya que proponia que se pueden obtener mejores resultados al primero analizar una matriz usuario-item que identifique relaciones entre items y luego basar la recomendación en esos resultados. También se menciona el tema de las complicaciones descritas en el paper principal, como la distribución de datos, carencia de estos y limitaciones de memoria.