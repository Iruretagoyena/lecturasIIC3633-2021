# Semana 2

#### Tema: Matrix Factorization Techniques
#### Entrega: 30 de Agosto, 8pm
Lecturas leídas:
- [x] Matrix factorization techniques for recommender systems.
- [x] Opcional: BPR: Bayesian personalized ranking from implicit feedback.

El resumen se basa en la lectura de Matrix factorization techniques for recommender systems y da algunos comentarios en base a comparación con una de las lecturas opcionales.

## Resumen semana 2

#### Introducción y Abstract

En esta oportunidad se analiza un artículo de revista publicado por en la IEEE Computer Society y escrito por investigadores de AT&T Labs. El articulo comienza hablando de la relevancia de los RecSys hoy en día, validados por su uso en Netflix y Amazon, compara las estrategias existentes para crear estos sistemas (content filtering y collaborative filtering). Luego de explicar los detalles de ambas tecnicas, ahonda en los dos principales metodos para hacer CF, "neighborhood methods" y "latent factor models", para luego basarsse en los factores latentes para explicar las tecnicas de factorizacion matricial y sus ecuaciones de minnimizacion, stochastic gradient descent y alternating least squares (ALS).

#### Comentarios personales y criticas acerca de las lecturas


En lo personal esta lectura me gustó un montón. Explica el panorama general de los RecSys hoy en día (bueno, más o menos, es del 2009 el paper original) y logra expresar el por qué son relevantes en la industria - cosa que creo no es tan trivial, o por lo menos no a la magnitud de tener secciones especiales en servicios gigantes como Youtube y Spotify.

No me gustá el uso de aristas "hombre vs mujer" para los experimentos. Self-explanatory. Se nota que es del 2009, hoy en día eso es funa directa. Hay otras mil dimensiones para separar personas.

Encontré pobre la sección que explicaba las formas de sobrellevar el "cold start" (página 46). Creo que queda muy al aire y solo menciona "buscar fuentes en otros lados". Podría haber dado más ejemplos de vida real, tipo "en este experimento hemos pedido datos de compañia X e Y".

Me gustó que ahondaran en las explicaciones matematicas de la factorización matricial de forma """simple""", o bien explicada al menos. Siento que quedó al aire el por qué menor RMS Error de los factores es mejor, y si se podría usar la conclusión inversa para determinar otras cosas (ej, recomendar cosas distintas a usuarios de perfiles "opuestos"). Encontré muy bueno que mencionasen el origen de la popularidad de los metodos estocasticos descendientes y el por qué ALS funciona mejor en algunos casos al aprovechar la convexidad de la ecuaciónn descrita (2). La convergencia de este método es la clave para su utilidad. Encontré genial además la sección de agregar bias con el ejemplo de Joe y el Titanic. Me gustaría ver explicaciones de como manejar ese bias en otros datasets, pero creo eso escapa de esta lectura.s

Los autores también fueron los que ganaron el Netflix Price con el equipo BellKor, explicando que en datasets como el que usaron, es posible utilizar factorizacion matricial obteniendo resultados muchisimo mejores que las tecnicas clasicas de nearest-neighbors. Ahí mencionan algo muy importante, esta técnica además es eficiente en memoria, lo cual es vital para el 99% de los desarrolladores que no tienen/quieren recursos de sobra para gastar en hardware (o en arrendar un servicio cloud). Poder obtener estos resultados de forma eficiente es lo que más me llama la atención. Eso si, me faltó la parte de "Future Work", en donde me hubiese gustado opiniones de los autores sobre en qué lineas se podría jugar para obtener mejores resultados, o poder procesar datasets más grandes (quizás no era preocupación el 2009 pero hoy si).