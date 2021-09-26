# Semana 6

#### Tema: Deep learning based recommender system: A survey and new perspectives. ACM Computing Surveys
#### Entrega: 27 de Septiembre, 8pm

- [x] Zhang, S., Yao, L., Sun, A., & Tay, Y. (2019). Deep learning based recommender system: A survey and new perspectives. ACM Computing Surveys (CSUR)

Link: https://arxiv.org/abs/1707.07435

- [x] Covington, P., Adams, J., & Sargin, E. (2016). Deep neural networks for youtube recommendations. In Proceedings of the 10th ACM conference on recommender systems (pp. 191-198).

https://dl.acm.org/doi/pdf/10.1145/2959100.2959190

## Resumen semana 6

#### **Lectura: Deep learning based recommender system: A survey and new perspectives.**

Este articulo busca ser un review comprehensivo del uso de deep learning en sistemas recomendadores, presentando una taxonomía de los modelos y resumen del estado del arte. El texto destaca a los RecSys como métodos efectivos contra el exceso de información, enalteciendo su potencial para resolver problemas que involucran selección de opciones, en general en un ambiente de consumidores vs productos.

Se presenta Deep Learning como una rama de Machine Learning, obteniendo su nombre debido a que genera 'representaciones profundas', i.e. múltiples niveles de representación y abstracción. Se mencionan MLP, AE, CNN, RNN, LSTM, RBM, NADE, AN, AM y DRL como técnicas.

Se justifica su uso debido a que las estructuras de información que analizamos en RecSys (i.e. sesiones, click-logs) son muy convenientes y a que podemos aprovechar la ventaja del aprendizaje de representación que nos permite mezclar distintas fuentes de información (imagenes, tweets, reviews, etc) para tomar decisiones.

Se mencionan ventajas como Nonlinear Transformation, Representation Learning, Sequence Modelling y Flexibility y desventajas como Interpretability, Data Requirement y Extensive Hyperparameter Tuning.

Luego se procede a dar conocimiento sobre el estado del arte en DL aplicado a RecSys, mencionando algunas de las técnicas y aplicaciones para ciertos casos.

Me llamó la atención el uso mencionado de CNN para introducir distintos tipos de fuentes como imagen, texto, audio y video. Se menciona el uso de CNNs en distintos ámbitos en donde podemos adaptar está técnica para extraer y aprender features, dandonos la posibilidad de "ensamblar" distintas fuentes, dando paso a un gran potencial de aprendizaje de máquina. Es interesante que menciona que las CNN se pueden utilizar directamente sobre Collaborative Filtering.

Siento que era una lectura no tan simple de opinar ya que eran más que nada técnicas concretas. Me gustó como se presentaba, entregando contexto y mencionando muchas fuentes de información con las que podemos trabajar usando DL, no solo basandose en texto y reviews. Creo que podrían haber sido más explicativos sobre las ganancias del DL en algunos casos, por ejemplo, mostrando efectividad en métricas de técnicas de Visión por Computador utilizando análisis de ventanas de pixeles versus alguna técnica de DL. CV es un área en donde el DL realmente irrumpió fuertemente y creo que no se presenta de forma tan obvia en esta lectura.

#### **Conexión con otras lecturas**

Como mencioné, me llamó mucho la atención que se resaltara la posibilidad de utilizar varias fuentes de datos para el mismo problema. Esto es exactamente lo que busca la Inteligencia Artificial, crear máquinas que logren ser realmente inteligentes, que entiendan el contexto y la situación. Hoy en día la mayoría de las máquinas que creamos se especializan en uno o pocos inputs, fijandose solo en el video o texto que le decimos que se fije. 

Tal como habíamos leído en la lectura de la semana pasada, Context-Aware Recommender Systems, en donde se busca integrar al contexto con el fin de obtener mayor riqueza de datos para la resolución del problema de recomendación, esta lectura nos da paso a la idea - "Y si pudiesemos crear una máquina que logre entender todo el contexto del problema, sin nosotros darselo ?".

Creo que el uso de DL y la inclusión del 'contexto' en la resolución de problemas es el mejor paso que hemos dado en la dirección de crear máquinas realmente conscientes, en donde puedan utilizar audio, video, texto y frecuencias para enfrentarse robustamente a ambientes cambiantes y de dificil adaptabilidad. Un buen momento para estar vivos y ver qué nos trae la innovación.

Por ejemplo, en el texto opcional de "Deep neural networks for youtube recommendations", se contruyen Watch Vectors, Search Vectors, información de edad, género y geolocalización que son consumisdas por una red de fully connected Rectified Linear Units para generar recomendaciones al usuario. Encuentro muy interesante todo lo que podemos mezclar. Esta área suele ser bien formal y matemática en su construcción y entendimiento, y creo que esto agrega una componente de ingenio/arte que aporta enormemente a la forma en que vemos e interactuamos con las máquinas.