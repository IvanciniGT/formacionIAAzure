                     Objetivo
PYTHON               Aprender a usar python para desarrollar apps sencillas.
PROCESS MINING       Aprender los conceptos básicos de PM y aplicarlos con python + PM4PY.
                     -> Objetivo de PM es poner foco sobre los procesos y cómo pueden mejorarse.
                     -> PRODUCTO: Un informe acerca del proceso de negocio que estamos analizando.
IA                   Aprender a crear apps tipo CHATGPT (más o menos)

CHATGPT es una IA? No es una IA.. es una aplicación tipo chatbot. 
Usa una IA para responder preguntas. Qué IA usa CHATGPT?
Hay un montón:
- GTP-3
- GTP-3.5
- GTP-4
- GTP-4 Turbo
- GTP-4 Turbo (GPT-4.5)
- GTP-5 (en desarrollo)
- O1
- O3

Eso de ahí arriba es lo que llamamos un MODELO de IA... en concreto modelos de tipo LLM (Large Language Model).

---
# IA

Programa que permite simular comportamientos inteligentes (como los que tienen los humanos).
Hay 2 formas de crear IA:
- Mediante programación tradicional (con reglas, condicionales, etc.). MUY POCO POTENTE.. son las típicas que creábamos hace 30 años... y aún hay alguna... pero pocas.
- Mediante aprendizaje automático (Machine Learning). Lo que hacemos es dejar a una computadora que genera un programa por sí sola, a partir de ejemplos/datos. 
  Esos programas que las computadora generan se llaman MODELOS. Y muchas veces (la inmensa mayoría) los humanos no somos capaces de entender cómo funcionan esos modelos (aún viéndolos por dentro).

Cuánto gasta un Ford focus de gasolina (cada 100Kms con una conducción normal) y un motor de 1.5 litros? 
- 6l

Cuánto gasta un BMW serie 5 de gasolina (3500cc) (cada 100Kms con una conducción normal)? 
- +10l

Estamos haciendo una predicción/estimación

Cuánto pesa un niño de 3 años? 
- 10-15 kgs <- Es otra predicción/estimación            12kgs

De dónde vienen esas respuestas? De los datos que hemos visto antes.

Una de las formas que tiene el cerebro humano para aprender es mediante datos.
No es la única. También puede por ejemplo aprender mediante razonamiento abstracto. Cosas de las que no ha visto información previamente... es capaz de predecir como funcionan (hipótesis). Eso luego puede comprobarlo con datos.

Al final... el aprender mediante datos no es sino aplicar técnicas estadísticas a los datos que tenemos.
Esto tiene algunas connotaciones:
- Cuantos más datos tengamos, mejor.... Más precisa puede ser la predicción.
Cuánto pesa un niño de 3 años, que es bajito y delgadito?
- 9-10kgs

A nuestros computadores, les dejamos crear esos programas, a partir de datos.
Pero... les damos algunas pistas/reglas acerca de cómo montar el programa.

Entre esas reglas por ejemplo, tenemos:
- El tipo de algoritmo que queremos usar (regresión lineal, regresión logística, árboles de decisión, red neuronal, etc.)
- Algunos de esos algoritmos necesitan de parámetros adicionales (más información) para funcionar. Por ejemplo, una red neuronal necesita de un número de capas y de perceptrones (neuronas) por capa.

Es igual que cuando voy a un arquitecto y le digo que quiero que me fabrique una casa.
El va a hacer el proyecto... pero yo le doy pistas/reglas de cómo quiero que sea la casa:
- Ladrillos de color rojo
- 3 plantas
- 2 habitaciones
- 136 m2

El arquitecto junto con su equipo de ingeniería, realizan el proyecto y luego la casa.
Si me pasan el proyecto... yo soy capaz de entenderlo? Partes si... otras posiblemente no.
Por qué se han hecho ciertos cálculos y no otros? de donde salen ciertos coeficientes?
Me falta conocimiento para entenderlo todo.

PERO el problema es SIMPLEMENTE que me FALTA CONOCIMIENTO.
Si tuviera ese conocimiento, podría entenderlo todo? SI

Con los modelos de IAs no pasa esto... No es problema de conocimiento. Es problema que de nuestro cerebro no da de si para manejar la cantidad de información que hay en esos modelos.

Un modelo grande... de estos que vamos a manejar... puede tener miles de millones de parámetros (coeficientes numéricos). Mi cerebro es totalmente incapaz de entender que significan esos números...
No ya porque el problema sea muy complejo (que lo es), sino porque son tantos números que no soy capaz de entenderlos. Lo más jodido... es que inconscientemente, mi cerebro funciona muy parecido a esos programas... Y aprende (se desarrolla) de una forma muy parecida a esos programas. Se usar mi cerebro... pero no soy capaz de entenderlo del todo.

Los modelos los usamos para:
- Clasificar cosas (por ejemplo, si una imagen es de un perro o de un gato. Otro ejemplo, en este texto que estoy leyendo, si es un texto de IA o no. Otro: Habla de algo positivo o negativo)
- Predecir resultados (por ejemplo, cuánto dinero me va a costar un asegurado de coche)
- Un uso de estos programas es GENERAR DATOS NUEVOS. Realmente esta es la novedad... Me refiero.. el resto de algoritmos los conocemos de hace décadas... Lo que pasa es que no había ni la capacidad de computación ni la cantidad de datos que hay ahora. Aún así se usaban mucho... (los otros)

Hoy en día... todas las IAs (todos esos modelos) se entrenan con un tipo de aprendizaje que se llama APRENDIZAJE PROFUNDO (Deep Learning). Y están basados en REDES NEURONALES (Neural Networks).

Hay empresas que se dedican a crear esos modelos. Las más conocidas son:
- OpenAI (GTPs, O1, O3, Dall-E, etc.)
- Google (Bard, Gemini, etc.)
- Meta (Llama, etc.)
- Anthropic (Claude)

También organismos tipo universidades, etc. (por ejemplo, la Universidad de Stanford ha creado un modelo llamado Alpaca).

Cuál es el principal problema para crear uno de esos modelos? 
- COSTE DE ENTRENAMIENTO
- TIEMPO DE ENTRENAMIENTO
    GPT-3.5 tardó 3 meses en entrenarse... y costó 100 millones de dólares (en gasto de alquiler de servidores, electricidad, etc.)
    GPT-3 era un modelo pequeño comparado con GPT-4.5 (que es el que se usa en ChatGPT).... Muy pequeño!
- TENER UN SET MASIVO DE DATOS... cada vez es menos problema... para las grandes organizaciones. Para una entidad pequeña... puede serlo.

Esto es un problema... Pocas empresas pueden permitirse crear un modelo de IA propio.
Y quién tenga hoy en día la mejor IA (o al menos una buena) tiene una ventaja competitiva enorme con respecto a empresas que no la tienen.

Cualquier red social!
- Youtube
- Facebook
- Instagram
- TikTok
- Twitter (X)
- LinkedIn

Todas la mierda que me van poniendo en la pantalla, quién la decide? una IA... que se ha entrenado para especializarse en mantenerme conectado a la red social.

Para una empresa pequeña.. que quiera crear su propia red social... es imposible competir con las grandes redes sociales. Es imposible! Como podéis imaginar ...las IAS (pasta) es un problema para la libre competencia. El crear un monopolio o un oligopolio es muy fácil... para las grandes empresas.. Siempre lo ha sido... pero ahora más que nunca.

Qué ha ocurrido.. que todas esas empresas (o la gran mayoría) han decidido abrir sus modelos de IA a la comunidad. En algunos casos de forma gratuita (OpenAI, Google, Meta, etc.) y en otros casos de forma de pago (Anthropic, etc.)... pero.. a precio amigo!

A mi... que tengo una empresa de venta de pescado... para que me sirve el modelo de identificación de personas en fotos de Meta? Y aquí es donde la cosa se pone turbia... porque me sirve un huevo... si lo sé usar.

---

# Vamos a intentar el día de hoy entender cuales son las bases de esos modelos... de las redes neuronales y del aprendizaje profundo.

- Perceptrón (simula el funcionamiento de una neurona). Qué es?
  Es una triste función matemática... con sus variables de entrada... y su resultado.

    y = sin(x) # Podría ser un perceptrón.

       Variables de entrada? x
       Resultado? y
    
    Lo que pasa.. es que en la realidad... los perceptrones se diferencian de esa forma matemática, en que tienen un montón de variables de entrada (x1, x2, x3, etc.) y una fórmula matemática mucho más compleja que la de esa ecuación.

  Lo que hace un perceptron al final es EXCITARSE O NO EXCITARSE.
  Eso algunos... otros SE EXCITAN UNA DETERMINADA CANTIDAD.

  Básicamente... de lo que estamos hablando:
  y = f(x1,x2,x3) -> 
    0       si no se excita
    1       si se excita
    0.3     si se excita un poco

Vamos a crear un perceptrón que sea capaz de simular un comportamiento humano... el comportamiento de la Y lógica .... AND

    ENTRADAS x1, x2
    x1: 0 o 1
    x2: 0 o 1

    SALIDA: y
    y = 0 cuando x1 o x2 son 0
    y = 1 cuando x1 y x2 son 1


Quiero saber si un vehículo es un coche o un camión.

- numeroRuedas >= 4            SI / NO   x1
- capacidadDeCargaAmpliada =   SI / NO    x2

Cuando sería camión ?  x1 AND x2
Una moto sería si:     NOT x1 ...

Los perceptrones son increiblemente buenos resolviendo problemas lineales.
Pero no valen para problemas no lineales.

Qué pasa cuando tenemos problemas NO LINEALES... Pues que no me vale un perceptrón... ni unos cuantos perceptrones.

Necesito una RED DE PERCEPTRONES.

    ENTRADAS        CAPA 1 de PERCEPTRONes    CAPA 2 de PERCEPTRONes    SALIDA

    X1  (0,1)  ----- AND \
                \ /       \
                 +         >-------------------- XOR  ---------------     0-1
                / \       /                                               
    X2  (0,1)  ------ OR /



                  AND   OR       XOR
   x1=0 x2=0 ->    0     0   ->   0
   x1=0 x2=1 ->    0     1   ->   1
   x1=1 x2=0 ->    0     1   ->   1
   x1=1 x2=1 ->    1     1   ->   0

Con una capa de perceptrones no puedo resolver problemas no lineales.
Y el problema es que la mayor cantidad de problemas que nos encontramos en la vida real son no lineales.
Para modelar esos problemas con perceptrones, necesitamos de varias capas de perceptrones.


RED NEURONAL PARA DETERMINAR Qué DIGITO HAY DIBUJADO EN UNA FOTOGRAFIA (0,1,2,3,4,5,6,7,8,9)

    SALIDA = 10 datos (0-9)
    ENTRADA?¿ Matriz de pixeles
    Si tengo una foto de 30x30 pixeles monocromo
    900 variables que pueden valer 0-1.
        (YA ES UN PROBLEMON)!!!
    
                CAPA 1 de PERCEPTRONES      CAPAS...                    SALIDA (La neurona que más se excite)
    x1                P1                                              n0
    x2                P2                                              n1
     .                P3                                              n2
     .                P4                                              .
     .                P5                                              n9
    x300
                      ^^^
                      APRENDIZAJE

    P1... sería una ecuación matemática que podría conceptualmente excitarse cuando? 
                Hay más pixels coloreados arriba que abajo
    P2... sería una ecuación matemática que podría conceptualmente excitarse cuando? 
                Hay más pixels coloreados a la izquierda que a la derecha
    P3... que hay pixels que por un lado no están conectados con otros pixels: Lineas que terminan
            1, 2, 3, 4, 5, 6, 7, 9
            Si hay una linea que termina: 9 o 6
            Si hay 2 lineas : 2, 4, 5, 7
            Si hay 3 lineas: 3, 1

    SI P1 no se excita que significa? Que no hay más pixels coloreados arriba que abajo (más o menos)
    SI P2 no se excita que significa? Que no hay más pixels coloreados a la izquierda que a la derecha (más o menos).
       Qué digitos cumplen eso? 0, 8   SI NOT P1 y NOT P2 -> 0 o 8
    
    Si hay má pixeles a la izquierda: 3 (NO) 9 (NO)

---

Cuántos pixels tiene una foto de un teléfono modernito?
Como poco 10MPixeles = 10.000.000 pixeles
O 25MPixeles = 25.000.000 pixeles

Cada pixel... lo represento con 3 colores: RGB (Rojo, Verde, Azul)

Dicho de otra forma en una foto de 10MPixeles tengo 30.000.000 de datos (10.000.000 de pixeles * 3 colores)
Donde cada variable puede variar entre 0-255.

UPS!!!!!
---


A qué llamamos un parámetro en una red:


                CAPA 1 de PERCEPTRONES      CAPAS...                    SALIDA (La neurona que más se excite)
    x1                P1                                              n0
    x2                P2                                              n1
     .                P3                                              n2
     .                P4                                              .
     .                P5                                              n9
    x300

    El valor x1 se pasa a cuántos perceptrones? a P1, P2, P3, P4 y P5 (5 perceptrones)
    En cada uno entra multiplicando por un valor (un parámetro)

    300 variables... dan lugar a 300x5 = 1500 parámetros (coeficientes numéricos) que son los que se van a ir ajustando durante el entrenamiento de la red neuronal.

    Cada perceptron... en su ecuación matemática, tiene un parámetro que se llama BIAS (sesgo).... suma a la ecuación.

    1500 + 300 = 1800 parámetros en total.

    Las salidas de los P1..P5 se mandan a los n0-n9 (la capa de salida).

    5 x 10 = 50 parámetros (coeficientes numéricos) que son los que se van a ir ajustando durante el entrenamiento de la red neuronal.
    Cada neurona de salida (n0-n9) tiene un BIAS (sesgo) que suma a la ecuación.
    50 + 10 = 60 parámetros en total.
    Total de parámetros de la red neuronal: 1800 + 60 = 1860 parámetros.


    Si las funciones matemáticas que se usaran fueran sigmoides (1/(1+e^-X)).

    La X de cada neurona P1...P5 sería:
    X = x1 * P1_x1 + x2 * P1_x2 + ... + x300 * P1_x300 + BIAS_P1
    X = 3.18x1 + 2.34x2 - ... + 0.12x300 - 0.5

    La neurona... su ecuación sería: 1/(1 + e^-(3.18x1 + 2.34x2 - ... + 0.12x300 - 0.5)) = P1
    P2 = 1/(1 + e^-(2.18x1 + 1.34x2 - ... + 0.22x300 - 0.3))
    P3 = 1/(1 + e^-(1.18x1 + 0.34x2 - ... + 0.32x300 - 0.1))
    P4 = 1/(1 + e^-(0.18x1 + 0.14x2 - ... + 0.42x300 + 0.5))
    P5 = 1/(1 + e^-(0.18x1 + 0.14x2 - ... + 0.52x300 + 0.7))
    n0 = 1/(1 + e^-(29.18P1 + 20.34P2 - ... + 0.12P5 - 0.5))
    n1 = 1/(1 + e^-(28.18P1 + 19.34P2 - ... + 0.22P5 - 0.3))
    n2 = 1/(1 + e^-(27.18P1 + 18.34P2 - ... + 0.32P5 - 0.1))

    Claro... cual es la mejor combinación de esos 1860 valores posible?

    De donde salen esos 1860 valores? Eso es el entrenamiento de la red neuronal.
    La red neuronal ... elige un conjunto de parámetros al azar (inicialmente) y luego los va ajustando para que dados unos datos de entrada YA CONOCIDOS, la salida sea la esperada para esos datos de entrada YA CONOCIDOS.

    Es decir, le paso 10.000 fotos de números escritos a mano (0-9) y le digo en cada foto que número hay (SALIDA REAL = salida esperada).

    RONDA 1: El programa inventa unos valores al azar para los 1860 parámetros.
    RONDA 2: Le paso las 10.000 fotos y el programa calcula la salida de cada foto (0-9) con los parámetros que ha inventado.
    RONDA 3: Compara la salida de cada foto con la salida esperada (la que le he pasado).
    RONDA 4: Calcula en cuantas fotos se ha equivocado (la salida no coincide con la esperada).
    RONDA 5: Ajusta un poquito los parámetros (coeficientes numéricos) a ver si la próxima vez que le pase las fotos, se equivoque menos. Que si.. sigue ajustando... que no ... ajusta para el otro lado

Y nosotros hemos planteado una red con 1860 parámetros... pero hay redes con decenas de miles de millones de parámetros.

Imaginad que el programa acaba... de calcular esos 1860 parámetros.... y nos dan los valores finales.

Al final.. prueba / error... prueba / error... prueba / error... acabamos con unos parámetros que nos dan una salida esperada muy buena.
Y listo.  Y que significan esos parámetros? Pues no lo sabemos... porque no somos capaces de entenderlos.

PERO... la realidad es que esto no es GPT... o cualquier otro modelo de IA.
Los modelos de IA que usamos son una parte de esa red neuronal que hemos entrenado... solo una parte... no la red completa.
---

Los modelos se ajustan / se entrenan con un conjunto de datos de partida: Datos de entrenamiento.
Qué pasa cuando quiero usar otro tipo de datos... O quiero producir una salida diferente?
Pues que tengo que ajustar el modelo a esos nuevos datos. Eso se llama AJUSTE FINO (Fine Tuning).

En muchos casos, básicamente se trata de entrenar una última capa de perceptrones (una capa de salida) que se ajuste a los nuevos datos.
Las capas intermedias se mantienen... Eso de hecho es lo que nosotros adquirimos o descargamos de los modelos de IA que usamos y que las empresas publican/entrenan y ponen a disposición de la comunidad: LAS CAPAS INTERMEDIAS.

Hay una página muy famosa con modelos de IA que podemos usar desde PYTHON: HUGGING FACE.

---

# Análisis de textos... Modelos LLM (Large Language Model)

Esto es lo que lleva dentro ChatGPT y GEMINI (Google).

Imaginad esta frase:

    "El perro de mi vecino es muy bonito"

¿Cómo hago que un modelo de IA entienda que significa la frase?

Si entiendo que significa, puedo:
- Clasificar la frase (es positiva o negativa)
- Puedo responder a preguntas sobre la frase (quién tiene el perro? qué tipo de animal es? etc.)

---
Habéis visto, que muchos de los modelos que hemos visto, ponía que se basan en el modelo Transformer.
Eso cambió todo en el mundo de la IA. Lo creo Google en 2017, y es cuando las IAs empezaron a ser realmente potentes.
Google decidió publicar ese modelo (es una arquitectura de red neuronal) y desde entonces, todos los modelos de IA se basan en ese modelo. Lo curioso es que ni siquiera llegamos a entender en profundidad como funciona ese modelo.

El paper original se llama "Attention is all you need" y lo podéis encontrar en Google.

---

Vuelvo al ejemplo de la frase:

    "El perro de mi vecino es muy bonito"


Lo primero que quiero es entender que dice esa frase.... y para ello, vamos a usar una red neuronal.
Ahora... las redes neuronales al final lo que tienen son perceptrones... que ya hemos visto que no son sino ecuaciones matemáticas.
A una ecuación matemática le puedo dar como entrada un texto? Una palabra? "perro"??? Hay que transformarla en algo operable matemáticamente.

Una forma básica de hacerlo es asignar un número a cada palabra.
Cuántas palabras hay en el diccionario? En español, podemos llegar casi al millón de palabras (teniendo en cuenta todas las formas de conjugación, plurales, diminutivos, etc.)

Claro.. eso me sirve para identificar una palabra... pero no me sirve para entender ni siquiera el significado de la palabra. No digamos el significado de la frase.

Qué es un significado? Y al final.. el significado de una palabra tiene que ver con las palabras con las que se relaciona.

Vamos a ver un ejemplo de palabras que se relacionan entre sí:

            Ser vivo    Comida    Objeto    Vehículo    Acción      PropioDePersonaHumana  (DIMENSIONES) Planta
Lechuga        1           1        0          0          0                0
Carne         0.4
Piedra
Tornillo
Bicicleta
Coche                                        
Rueda                                        
Comer         0            0.5      0        0          1                  1

Esas relaciones, que puedo cuantificar en intensidad son las que me permiten entender el significado de una palabra.

En la realidad lo que hacemos es crear un VECTOR de palabras. Cada palabra tiene un vector.
Cada posición de ese vector es una dimensión a la que la palabra se asocia.

Qué dimensiones pongo? 20, 50, 500? Cuales son? Eso ya es un problemón en si mismo.
De hecho esto ya no lo hacemos los humanos... lo pido a una computadora. 
Toma un corpus de palabra (hoy en día tenemos millones de libros, artículos, noticias, videos...) Y mira a ver qué palabras se relacionan entre sí. Cuales pueden aparecer como sustitutos de otras, etc.

Y dejo a la computadora que elija las dimensiones y los valores de cada dimensión. Yo le doy en # de dimensiones que quiero y le dejo que elija los valores de cada dimensión.... y el resultado es un VECTOR con puntuaciones para dimensiones que no tengo npi de lo que son.. no las putuaciones... sino ni siquiera las dimensiones.

Ese vector, lo que contiene es en esencia el significado de la palabra.

Y si aplico el mismo procedimiento por ejemplo a corpus de distintos idiomas? Pues obtengo un vector de palabras en cada idioma.

   Perro (español) -> [0.1, 0.2, 0.3, 0.4, 0.5]
   Dog (inglés)    -> [0.1, 0.2, 0.3, 0.4, 0.5]

De ahí vienen los procedimientos (y modelos) de traducción automática.

2 palabras que tengan puntuaciones muy similares en sus vectores, son palabras que significan lo mismo o muy parecido.
2 palabra completamente alejadas en sus vectores, son palabras que no tienen nada que ver.
2 palabras que tengan casi todas las puntuaciones iguales, menos  1 o 2 podrían ser antónimos.

grande , pequeño, frio

Cada palabra se transforma en su vector de puntuaciones.
Y eso es lo que entra al modelo de IA ( a la red neuronal).

Luego viene la red neuronal.. que hoy en día están basadas en el modelo Transformer.
De qué va eso:

 Lo que se hace es mirar la frase en su conjunto, y ver cómo se relacionan las palabras entre sí.

      +-----------+
      |           |
      v           |
    _________ ____________
    "El perro de mi vecino es muy bonito"       "El cánido del que vive a mi lado es super chulo"
     |   ^      20 números      más o menos iguales a          20 números
     +---+

     El y Perro aparecen muchas veces juntos en la literatura.
     El y Bonito aparecen muchas veces juntos en la literatura.... pero menos
     Muy y bonito aparecen muchas veces juntos en la literatura.
     perro y muy aparecen algunas veces juntos en la literatura.
     perro y vecino aparecen algunas veces juntos en la literatura.
---

Una cosa es entrenar un modelo... que lleva meses
Otra cosa es usar un modelo ya entrenado... que lleva de milésimas de segundos a minutos.. o a horas.

Para muchas cosas, con modelos sencillos nos vale... y tardarán muchísimo menos en ejecutarse.
Y si lo voy a ejecutar millones de veces... pues mejor que sea rápido.... No solo por el tiempo...  sino por la pasta que me cuesta ejecutar el modelo.



    100x100            RED

    100.000 pixels     300  >  50  >  20  > 50 > 300 -- > 100.000 pixels
    contexto >                        --------------
                                      Modelo generativo
                                      Le meto 20 datos aleatorios y genera una foto.

    Y entre no la red de forma que las ecuaciones matemáticas que se generen consigan que la salida sea la misma que la entrada

    En el ejemplo de google colab. Se aplica otra forma de crear ese modelo: GAN: Generative Adversarial Network
    Se entrenan 2 redes neuronales:
    - Una red que genera fotos partiendo de datos aleatorios (la generativa)
    - Una red se alimenta con fotos generadas al azar y generadas por humanos (de la BBDD - la discriminativa)
    - Y se entrenan juntas poniendose a competir entre si.
     - La primera, su objetivo es conseguir engañar lo más posible a la segunda.
     - La segunda, su objetivo es conseguir detectar las fotos generadas por la primera y no por un humano
   Una vez entrenadas, tiro la discriminativa y me quedo con la generativa. 


   Frase con hasta 1000 palabras. -> 1000 datos de entrada
   300 neuronas en capa 1 = 1000x300 + 300 = 300.300 parámetros
   Si meto 50 neuronas en capa 2 = 300x50 + 50 = 15.050 parámetros
   Si meto 20 neuronas en capa 3 = 50x20 + 20 = 1.020 parámetros
   Total = 300.300 + 15.050 + 1.020 = 316.370 parámetros

   Los modelos de IA avanzados tienen decenas de miles de millones de parámetros.
    17.000.000.000

Imaginad la cantidad de neuronas y capas que tienen esos modelos.

Lo que hacemos nosotros es coger uno de esos modelos... y particularizar su caso de uso:
Dicho de otra forma: Añadir unas capas de neuronas al final (desde las dimensiones latentes) que se ajusten a nuestro caso de uso:
- Clasificar
- Agrupar
- Predecir
- Generar

En muchos casos, no hacemos ni eso!
No merece la pena..
Si quiero generar una red neuronal que sea capaz de responder a preguntas (de una BBDD mia de preguntas).. Ya hay mucha gente en el mundo que ha hecho eso. Que ha entrenado esa segunda parte de la red neuronal... para este uso concreto.

Si quiero generar una red neuronal que sea capaz de identificar objetos en fotos (de una BBDD mia de fotos).. Ya hay mucha gente en el mundo que ha hecho eso. Que ha entrenado esa segunda parte de la red neuronal... para este uso concreto.

Lo único que tengo que hacer es darle a esa red neuronal mi BBDD de fotos o preguntas y respuestas, y ajustarle un poquito los parámetros de la red neuronal para que con mis datos se obtengan buenas respuestas.

Y esto es lo que hacemos hoy en día.... a no ser que me invente un caso de uso que no se le haya ocurrido a nadie en el mundo antes que a mi...
LO CUAL ES ALTISIMAMENTE IMPROBABLE.

Y eso es lo que me da MICROSOFT AZURE en el IA FORGE.

Le digo el caso de uso (y de ahi MS tiene preseleccionados las redes neuronales que mejor vienen a ese caso de uso) y le digo los datos que tengo (mis preguntas y respuestas, mis fotos, etc.) y el me ajusta la red neuronal para que con esos datos obtenga buenos resultados.

Evidentemente, o le doy muchos datos... o no voy a conseguir buenos resultados.

Esto mismo lo podríamos hacer a pelo con python... descargando los modelos de HUGGING FACE y ajustándolos a nuestros datos.
Microsoft em regala ese trabajo... Regala = €€€€€

A lo mejor pienso... YO NO SOY TONTO... pa' que voy a pagar si lo puedo hacer yo.
Pero no es solo crear el modelo.. o mejor dicho, afinar el modelo.
Por otro lado hay que coger ese programa que se ha creado e instalar en un servidor. Y Microsoft (AZURE) también me pone la máquina.
Y esa máquina hay que instalarle un SO... y python.. y librerías.. e ir actualizándole las versiones de py, librerías, y del SO... (Y eso me lo hace Microsoft)

Y Al final... pues es echar cuentas.

Si me decido (el core de mi negocio) es crear modelos de IA... pues me monto mi infraestructura y me pongo a ello.
Pero si no es el core de mi negocio... pues pago a Microsoft y me olvido de todo eso.

Y lo hace Microsoft en azure.. y lo hace Amazon en AWS y lo hace Google en GCP y lo hace IBM en su nube y lo hace Oracle en su nube y lo hace Alibaba en su nube.


# AZURE
El cloud de Microsoft

# AWS
El cloud de Amazon

# GCP
El cloud de Google

# Cloud?

El conjunto de servicios que una empresa de IT ofrece a sus clientes a través de internet.... de forma automatizada y mediante un modelo de pago por uso.

---

Vamos a montar un bot conversacional (algo así como un chatgpt) que sea capaz de responder a preguntas sobre un conjunto de datos que le pasemos.

Va a ser muy sencillo... me lo dan todo hecho.

Lo único que necesitamos es un buen conjunto de preguntas y respuestas.

Vamos a imaginar una empresa de venta de: Tractores

Para cargar preguntas, tenemos varias opciones:
- Crearlas a mano dentro de el Language Studio de Azure
- Cargar un fichero de preguntas y respuestas (CSV, JSON, txt, etc.)
- Pasa runa URL de un sitio web donde estén las preguntas y respuestas (un FAQ por ejemplo)
  ^ Si tengo algo como eso... buen sitio para empezar  

Lo primero si tengo un una web, de ahí quizás pueda rascar las preguntas y respuestas.
Después, lo que haremos siempre es preparar un fichero de preguntas y respuestas (CSV, JSON, txt, etc.) que subiremos a Azure.

En ocasiones hay que cubrir lagunas... o dar formulaciones alternativas a las preguntas que ya tenemos.


---

En muchos bots, podemos añadir la opción de Chit-Chat.

Si no lo añadimos, el bot solo responderá a las preguntas que le hemos cargado.
Si alguien pregunta algo del tipo:
Buenos días, que tal?
El bot no sabrá que responder. No tiene información para eso.

La opción de chit-chat nos permite soporte para conversaciones banales... pero más humanas

---


URL del servicio REST: 
https://preguntas.cognitiveservices.azure.com/language/:query-knowledgebases?projectName=QA-Tractores&api-version=2021-10-01&deploymentName=test

CURL está guay para pruebas automatizadas... y veremos ejemplo de cómo usarlo con python.

curl 

-X POST 

"https://preguntas.cognitiveservices.azure.com/language/:query-knowledgebases?projectName=QA-Tractores&api-version=2021-10-01&deploymentName=test"

 -H "Ocp-Apim-Subscription-Key: 2Tuw3uFSw988wcGtLnrPpc19B8fOtQspTodpx9KJq9akpc3zeZ7wJQQJ99BFACYeBjFXJ3w3AAAaACOGGjOy" 
 -H "Content-Type: application/json" 
 
 -d "
    {
        "top": 3,
        "question": "YOUR_QUESTION_HERE",
        "includeUnstructuredSources": true,
        "confidenceScoreThreshold": "YOUR_SCORE_THRESHOLD_HERE",
        "answerSpanRequest": {
            "enable": false,
            "topAnswersWithSpan": 1,
            "confidenceScoreThreshold": "YOUR_SCORE_THRESHOLD_HERE"
        },
        "filters": {
            "metadataFilter": {
                "logicalOperation": "YOUR_LOGICAL_OPERATION_HERE",
                "metadata": [
                    {
                        "key": "YOUR_ADDITIONAL_PROP_KEY_HERE",
                        "value": "YOUR_ADDITIONAL_PROP_VALUE_HERE"
                    }
                ]
            }
        }
    }


Para pruebas manuales, podemos usar un cliente para peticiones REST: Extensión de chrome (firefox): Boomerang REST API Client

---

El día 1, montar un chatbot (o cualquier otro tipo de programa de IA) y que ofrezca buenos resultados es complejo... Tarea IMPOSIBLE!!!
Se la dejamos a ITHAN HUNT (el de la película Misión Imposible) y a su equipo de hackers.

Estos programas hay que irlos retroalimentando... en nuestro caso (el chatbot de preguntas y respuestas) con nuevas preguntas y respuestas... o con más variantes de las preguntas que ya tenemos.

---

Nuestra base de preguntas y respuestas, es básicamente el código que escribimos para crear el chatbot.

Lo ideal es esa base de preguntas y respuestas tenerla controlada en un repositorio de código (GitHub, GitLab, Azure DevOps, etc.).
Idealmente, lo que haremos será que cada vez que publiquemos un nuevo conjunto de preguntas/respuestas (una nueva versión), se despliegue automáticamente en el servicio de Azure (DEVOPS).

# DEVOPS?

Metodologías ágiles (SCRUM, KANBAN, EXTREME PROGRAMMING, etc.) esos son metodologías de gestión de proyectos de desarrollo de software.

Devops es otra cosa. Es una cultura... un movimiento... una filosofía... en pro de la AUTOMATIZACION de trabajos entre el DEV ---> OPS.
- Integración Continua
- Entrega Continua
- Despliegue Continuo

# MLOPS?

Es una extensión de DevOps para el mundo de la IA.
Querremos que de una BBDD se genere automáticamente un modelo de IA, que se entrene y se despliegue en producción.
Y que recopilando datos de uso, se pueda ajustar el modelo de IA y volver a desplegarlo en producción.

Todo en automático.. o al menos lo más que pueda.