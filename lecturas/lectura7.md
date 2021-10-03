# Semana 7

#### Tema: Interactive recommender systems
#### Entrega: 4 de Octubre, 8pm

- [x] He, C., Parra, D., & Verbert, K. (2016). Interactive recommender systems: A survey of the state of the art and future research challenges and opportunities. Expert Systems with Applications, 56, 9-27.

- [x] Andjelkovic, I., Parra, D., & O’Donovan, J. (2019). Moodplay: Interactive music recommendation based on Artists’ mood similarity. International Journal of Human-Computer Studies, 121, 142-159.

https://dl.acm.org/doi/pdf/10.1145/2959100.2959190

## Resumen semana 7

#### **Interactive recommender systems**

El paper de esta semana presenta distintos temas tangentes al problema de recomendación. Se pone hincapié en factores humanos intrínsecos de esta operación, como la confianza de la persona, su satisfacción, la transparencia de la recomendación y el sentido de control que se obtiene al trabajar en esta área de conocimiento y no tanto a la precisión del resultado final.

Se presenta un framework de visualización que une sistemas recomendadores con técnicas de visualización, dando paso a la posibilidad de tener interacción humana que incida en el proceso de recomendación.

Me gusta que resalté la esencia de los RecSys y el por qué son útiles; nos ayudan a resolver el problema del exceso de información y opciones al momento de querer maximizar el valor entregado al usuario, tanto en experiencia como en tiempo invertido. Eso sí, es cierto también que estos sistemas presentan problemas intrínsecos como su inhabilidad de poder recomendar a usuarios o items nuevos de los que no tenemos información (cold start) o su funcionamiento de baja explicación (black box), como también la falta de feedback del usuario sobre las recomendaciones entregadas. De estas falencias se introduce el interés de l@s investigador@s en desarrollar técnicas que mezclen sus sistemas con interacción humana, por ejemplo, usando visualizaciones que permitan transparentar y controlar el proceso de recomendación. Esta mezcla busca solucionar el problema de transparencia, aumentar el control del usuario, la falta de diveridad, los problemas cold start y promover la adquisición y representación de información de contexto. Creo que el método que se presenta es interesante e innovador, no se me había ocurrido algo similar hasta este punto en el curso.

Encontré muy interesante el desarrollo de la idea de "contexto" en sección 2, Background, pg. 10 y el como se expande la definición general con la intuición de integrar perspectivas sociales y tecnologicas. Por ejemplo, incluir el clima en una recomendación podría incidir en ofrecer chocolate caliente en un día lluvioso, o helados en uno caluroso, lo cual crea sistemas mucho más inteligentes y adaptativos.

El paper luego empieza con una dinámica muy interesante. Juntados por objetivos, se presentan distintas investigaciones y sus métodos empleados para lograr tal objetivos. Los objetivos son transparencia, justificación, controlabilidad, diversidad, cold start y contexto. Quedé sorprendido de lo completa que era la lista, citando muchísimos papers recientes y dando una muy buena contextualización, no soslo del estado del arte, si no de qué cosas están buscando con esas investigaciones y cómo lo hacen. Me gustó mucho esta parte ya que era tremendamente completa, dando muchos ejemplos concretos, en donde la gran mayoría no me eran conocidos.

No solo eso, si no que el paper se empieza a poner aún más completo. Se empieza a detallar un análisis, también segmentado por objetivo, en donde se analiza las técnicas de visualización y qué métodos específicos fueron usados, además de las métricas de evaluación en las que se basaron para medir impacto. Me gustó mucho la Tabla 2, "Evaluations of interactive recommender systems" ya que visualiza concretamente las diferencias y similitudes de cada investigación. Creo que nunca había visto un desglose de survey de tal forma, y creo que es tremendamente útil para saber "donde estamos parados" en el área. Personalmente encontré que la página 21 estaba un poco colapsada con imágenes y rompía un poco el esquema seguido en el resto del paper (que puede ser bueno o malo, según lector). En la página 24, eché de menos que hubiese más información con respecto a la privacidad, que es un tema que personalmente me gusta.

Concuerdo fuertemente con uno de los puntos de la conclusión, "as advanced visualizations may be too complex for a wide audience.", ya que  generalmente trabajamos con gente que está acostumbrada al uso de gráficos y herramientas tecnologicas, y esto claramente no es cierto en todos lados, por lo que ahí existe una componente importantisima en el desafío de estas técnicas. Cómo permitir la interacción con usuario, pero a la vez no dejarlo atrás al usar métodos muy complejos ?

Por último, creo que esta investigación es tremendamente útil para la gente que quiere investigar el área de RecSys, y me atrevería a decir que para cualquier persona que quiera hacer investigación. Este survey es pontetisimo y presenta una sistematización en la comparación de métodos e investigaciones, que no me cabe duda que tuvo una enorme inversión de recursos detrás.

#### **Conexión con otras lecturas**

Lectura opcionl leída

- Andjelkovic, I., Parra, D., & O’Donovan, J. (2019). Moodplay: Interactive music recommendation based on Artists’ mood similarity. International Journal of Human-Computer Studies, 121, 142-159.

De todas las lecturas opcionales que leí, esta fue la que más correlación tenía con la principal, calzaba como anillo al dedo. Esta lectura se centra de igual manera en la estructura holistica de los sistemas recomendadores y su objetivo. Se habla del procesos y de sus tangentes de transparencia, explicación de resultados, control y experiencia de usuario. Me gustaron un montón estas lecturas ya que es típico leer miles de papers que buscan combinar métodos de forma distinta al estado del arte, con el fin de mejorar un 0.000001 el resultado. Estos no. Estos papers tienen una mirada desde arriba sobre que se está haciendo y lo presentan de una forma atractiva.

Ahora bien, este paper opcional iba un paso más allá. Presentaba una visualización interactiva que soporta la operación de recomendación. En unn mapa que denota "sentimientos" y artistas musicales en un espacio 2-D. 

Algo interesante me pareció que fue la presentación de resultados empíricos acerca de la cantidad de información desplegada por esta herramienta. Encontré que era algo clave, ya que puede ser muy factible que nuestra visualización agregue mucha información muy relevante, pero si saturamos al usuario, tendremos experiencia negativa y nadie usará la herramienta. Es por esto que me pareció un factor clave la integración de esta arista.

El paper se encarga de presentar una introducción correcta al tema. Qué se ha visto hasta ahora ? De qué forma ? Esto nos ayuda a entender el cómo se dió paso a esta idea y por qué es relevante en el área. Se justifica su diseño siguiendo el mantra “Overview first, zoom and filter, then details on-demand”. En general, cada paso de la formación de esta visualización está documentada, desde de a donde sacaron los datos, los algoritmos, en qué afecta el humor de la persona en la recomendación, etcera.

Me gustó un montón la "Trail-based recommendation" ya que encontré  muy interesante el hecho de involucrar sentimientos o humor actual en la recomendación. Esto es exactamente lo que queremos lograr con IA, crear máquinas inteligentes que entiendan contexto. Los resultados de la investigación se presentan de forma muy completa y segmentada según tema. Generalmente los papers juntan sus conclusiones en una sola sección y creo que no se aprovecha. Este paper lo muestra de muy buena forma. Se presenta una sistematización para evaluar resultados, evaluar percepción de usuario, la efectividad de la técnica, entre otros.

Concuerdo con que un desafío importante es la reducción de dimensionalidad en los sentimientos/artistas. Cómo mapeamos correctamente la cantidad y tipos de humores a un artista determinado ? Creo que esta es una arista importante que podría influir fuertemente en la efectividad del método.