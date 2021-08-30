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

Encontré pobre la sección que explicaba las formas de sobrellevar el "cold start" (página 46).

Me gustó que ahondaran en las explicaciones matematicas de la factorización matricial de forma """simple""", o bien explicada al menos. Siento que quedó al aire el por qué menor RMS Error de los factores es mejor, y si se podría usar la conclusión inversa para determinar otras cosas (ej, recomendar cosas distintas a usuarios de perfiles "opuestos").
