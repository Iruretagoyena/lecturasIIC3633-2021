# Semana 3

#### Tema: Evaluating recommendation systems
#### Entrega: 6 de Septiembre, 8pm
Lecturas leídas:
- [x] Guy, S., & Gunawardana, A.. (2011) “Evaluating recommendation systems.” In Recommender systems handbook, pp. 257-297. Springer US, 2011.
https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.712.4138&rep=rep1&type=pdf

- [x] Cremonesi, P., Koren, Y., & Turrin, R. (2010). Performance of recommender algorithms on top-n recommendation tasks. In Proceedings of the fourth ACM conference on Recommender systems (pp. 39-46). ACM.
https://dl.acm.org/doi/pdf/10.1145/1864708.1864721

## Resumen semana 3

#### **Introducción y Abstract**
El paper de esta semana trata sobre los métodos de evaluación de sistemas recomendadores, desde sus entornos a sus mediciones matemáticas para compararlos.
Basados en comparación de tres escenarios (offline setting, user studies y large scale online experiments) y distintos algoritmos, se compara cada opción, mencionando las ventajas y desventajas de cada uno, en cada ambiente. 

Se intenta utilizar metodos de comparación efectivos, mencionando que un benchmark absoluto no es consistente en todos los casos. La lectura es muy completa e interesante, menciona muchos ejemplos concretos y busca construir una composición para comparar y evaluar modelos de recomendación según distintos contextos.

Los tres 'settings' que se utilizan son:
- offline: sin interacción  de usuario
- user storiess: small group 
- large scale online distributed system, usuarios reales interactuando con el sistema, incluso en desconocimiento de parte del usuario

Luego se procede a hablar de distintas métricas matemáticas que sirven para comparar, y de conceptos claves para entender estos sistemas.

Muy buena lectura. Me costó un poco por su extensión y nivel de detalles, pero ha sido mi favorita hasta ahora dado  que encapsula el espectro de problemas de forma interesante y detallada. Incluso, preferí entregar mi análisis un poco más tarde para poder re-leer la lectura, ya que sentí que la primera vez no entendí el 100% de lo que abarca.

#### **Comentarios personales y criticas acerca de las lecturas**


Me gustó al inicio que comentase sobre

1. "Users may also be interested in discovering new items, in rapidly exploring diverse items, in preserv- ing their privacy, in the fast responses of the system, and many more properties of the interaction with the recommendation engine"

 y más adelante con comentarios como 

 2. "In many applications people use a recommendation system for more than an exact anticipation of their tastes. Users may also be interested in discovering new items, in rapidly exploring diverse items, in preserv- ing their privacy, in the fast responses of the system, and many more properties of the interaction with the recommendation engine" 

 - Encontré muy importante estas aclaraciones que se hacen (varias veces) en el paper. Personalmente solía creer que los RecSys tenían aplicaciones limitadas y este tipo de aclaraciones me permitió ver que se puede analizar en distintos escenarios y utilidades.

"If we train A on the MovieLens data set, and B on the Netflix data set, and algorithm A presents superior performance, we can not tell whether the performance was due to the superior CF model, or due to the better input data, or both. As the goal of the offline evaluation is to filter algorithms, the data used for the offline evaluation should match as closely as possible the data the designer expects the recommender system to face when deployed online." Ya, genial, si de acuerdo, pero como ??? Quizás quedó un poco al aire y solo se menciona "particiona bien sin bias". Más fácil decir que hacerlo.

"The online book retailer Amazon2 provides average user ratings for displayed books, and a list of other books that are bought by users who buy a specific book. Microsoft provides many free downloads for users, such as bug fixes, products and so forth." - Esta seccion está muy buena ya que aterriza estos temas a la industria y muestran claramente el por qué son relevantes hoy en día.

"For example, we can check an e-commerce website revenue with and without the recommender system and make an estimation of the value of the system to the web- site."  Mhh no lo sé, Rick. No sé si es posible determinar de esta forma, me hubiese gustado ejemplos reales de valorizaciones de start ups netamente basados en sus RecSys.

"For example, it is well known that paid subjects tend to try and satisfy the person or company conducting the experiment." Clave esta aclaración, si tenemos testeo de usuarios pagados, puede que aún así la info venga con bias, lo que podría hacer que la inversión en testeo no se justifique.

Me gustó que detallasen tecnicas para medir la confianza en distintos escenarios con distintas distribuciones (se menciona normal y gamma) pero creo que lo dejaron con muy poco detalle y podrian haber hablado sobre inferencia estadistica sobre los datos.

Me gustó también que la lectura fuese exhaustiva en las formas matemáticas actuales para comparar modelos, como Precision, Recall, RMSE, MAE etc. También encontré interesante la sección de Rankins y sus tipos. Creo que la última sección, en donde habla de Risk, Robustness, Utility, Diversity y Serendipity es muy completa y da un barrido general a los keywords que alguien que trabaja en esta area DEBE conocer. Eso si creo que en Privacidad podrían haberse explayado un poco más. Creo en general que la lectura es muy completa y una que alguien que quiere meterse en el area debe leer si o si. Buena elección.


