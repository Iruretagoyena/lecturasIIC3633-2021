# Semana 5

#### Tema: Context-Aware Recommender Systems + Combining predictions for accurate recommender systems.
#### Entrega: 20 de Septiembre, 8pm (Extensión hasta 22 de Septiembre)

 - [x] Adomavicius, G., Mobasher, B., Ricci, F. and Tuzhilin, A. (2011). Context-Aware Recommender Systems. AI Magazine, 32(3), 67-80.

Link: https://ojs.aaai.org//index.php/aimagazine/article/view/2364

 - [x] Jahrer, M., Töscher, A. and Legenstein, R. (2010). Combining predictions for accurate recommender systems. In Proceedings of the 16th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, 693-702. ACM. Sugeridas

Link: https://dl-acm-org.pucdechile.idm.oclc.org/doi/10.1145/1835804.1835893

Sugeridas

 - [ ] Pigi K., Shobeir F., James F., Magdalini E. and Lise G. (2015). HyPER: A Flexible and Extensible Probabilistic Framework for Hybrid Recommender Systems. In Proceedings of the 9th ACM Conference on Recommender Systems (RecSys '15), 99–106. ACM.

 - [ ] Rendle, S. (2010). Factorization machines. In 2010 IEEE International Conference on Data Mining (pp. 995-1000). IEEE.


## Resumen semana 5

En esta oportunidad, decidí leer los dos papers principales recomendados, buscando dar una breve intro a cada uno y una opinión personal que mezclase ambos.

#### **Lectura 1: Combining predictions for accurate recommender systems**

Este interesantisimo paper trata de la combinación de modelos de filtrado colaborativo con el fin de obtener mejores resultados que cualquiera de esos modelos por si solos. El paper se refiere a esa combinación como 'model blending'.

Se presenta una sistematización empírica de distintos 'blends', todos entrenados con el mismo dataset utilizado para el conocido 'Netflix Price' (ya lo hemos visto varias veces en clases por lo que evitaré explicaciones de que es el concurso). Algo entretenido de este sistema presentado es que no ssolo sirve para modelos de filtrado colaborativo, si no que busca ser un sistema para problemas de regresión supervisada en general.

Se comienza setteando el 'common ground', explicando cómo los algoritmos de CF utilizan historial de eventos usuario-item para predecir eventos futuros. Se presentan varios algoritmos conocidos que utiles para el problema (Knn item-item, Knn usuario-usuario, SVD)  y otros no tan frecuente como máquinas Boltzmann y AFM.

Algo muy interesante (en mi opinión) que hacen es el uso de combinación de modelos por medio de "Residual Training", el cual entrena i modelos basandose en los errores de los modelos anteriores. Personalmente nunca había leído de esa aplicación en algoritmos de CF, por lo que me pareció genial.

Para la evaluación de 'blendings', se comienza con un método linear, para luego probar binned blending,Gradient boosted decision trees, neural networks, k-nearest neighbors algorithm y kernel ridge regression.

El algoritmo BGBDT - Bagged Gradient Boosted Decision Tree me pareció extremadamente ingenioso, ya que logra sobrellevar el problema planteado de el output discreto de un árbol de decisión. Además, me gustó mucho que se indicase notación Big O de los algoritmos como forma de justificar por qué Kernel Ridge y KNN eran demasiado lentos y por eso usaban particiones del dataset.

Algunas notas,

1. Página 694, Tabla 1, comentario "Red values are critical for large scale applications." Critical en qué sentido ? Muy malos ? Buenos ? No me queda claro el comentario.

2. Personalmente no estaba familiarizado con 'out-of-bag estimate' y lo tuve que buscar. Siento que podría haber sido explicado.

3. Me hubiese gustado una explicación de por qué basan todos sus análisis en el RMSE.

4. Página 699, sobre los 'Bagged Gradient Boosted Decision Tree', se comenta "A good value to start with is the square root of the number of features.". Por qué es eso un buen valor ?



#### **Lectura 2: Context-Aware Recommender Systems**

Empezando con una levemente filosófica proposición del verdadero significado de 'contexto', este paper busca introducir los Sistemas Recomendadores que buscan conocer el contexto de la información que manejan con el fin de dar mejores recomendaciones.

Se proponen dos aspectos principales,
- Lo que el RecSys sabe acerca de los 'factores de contexto'  (i.e. tiempo, lugar, propósito).
- Cómo cambiane en el tiempo estos factores.

Se define también el tipo de conocimiento sobre estos factores (completamente observable, parcialmente observable y no observable), lo cual da paso a la discusión de cómo estos cambian en el tiempo (estáticamente o dinámicamente).

Se oficializa la diferencia de la representación de los sistemas tradicionales versus los basados en contexto, en donde los tradicionales buscan estimar una función de rating

R : Users x Items - Ratings

Mientras que los de contexto,

R : Users x Items x Contexts - Ratings

Obteniendo una mayor dimensionalidad del problema, asumiendo que los items no son consumidos de forma aleatoria, si no que dependen de un contexto adyacente. Eso si, cabe mencionar que el paper deja en claro que existe información tanto explícita como ímplicita sobre el contexto, i.e. saber si una persona está en un sitio web de e-commerce para comprar algo para su trabajo o su pareja, basado en aprendizajes de modelos anteriores (ej, tiempo del año en que lo compra - 'es cerca del aniversario ?').

Es muy interesante la formalización de los paradigmas sobre la inclusión del contexto dentro del sistema, dividiendo en prefiltrado, postfiltrado y modelaje por contexto. Dependiendo del objetivo, se utiliza el contexto antes, despúes o en su construcción basal. Según el caso, se da lugar a nuevas optimizaciones y formas de obtener mejores resultados, como el uso de sistemas conversacionales o adaptativos, que utilizan información que podría parecer no directamente relacionada para optimizar la experiencias de usuario. Me pareció genial esta sección del paper, ya que da ejemplos muy concretos y variados sobre estas aplicaciones (como el mood del usuario para la música, o la ubicación geográfica para optimización de búsqueda en la app). Ahora bien, queda muy abierto el tema con respecto a cual es mejor en cada caso (incluso esto se menciona como desafío al final del paper), lo que sería muy interesante para ahondar en otra lectura.


#### **Opinión personal sobre ambos textos**

Algo que me llamó mucho la atención luego de leer ambas lecturas fue  el hincapié que se le hace al "ensamblaje" de técnicas. Ambos papers aluden a la posibilidad de mezclar distintas herramientas con el fin de obtener mejores resultados.

Esto plantea un nuevo desafío para la persona que busque investigar o enfrentar un problema específico. Ya no solo trata de conocer un amplio set de herramientas, si no que debe manejarlas al punto de saber en qué momento va a ser mejor una, y en qué contexto será mejor la otra.

También es positivo, ya que permite expandir las opciones y permitir un approach más rico y completo para solucionar nuestro problema. Si bien ambas lecturas hablan de dominios distintos (uno sobre el contexto y el otro de ensamblaje de modelos), los dos apuntan a esta posibilidad, dando muy buenas referencias y formalizaciones para enfrentar las situaciones del día a día.

Personalmente me gustó más la segunda lectura, sobre contexto, ya que sentí que entregaba una visión más global del problema, dando varios ejemplos y contextos (jaja) en donde se utilizan estos paradigmas, mientras que el primero era muy enfocado a un dataset específico (el del Netflix Price).
