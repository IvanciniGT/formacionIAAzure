# Metodologías ágiles

**El objetivo de las metodologías ágiles es ir entregando el producto de forma incremental.**

Son una evolución de las, hoy en día, llamadas metodologías tradicionales. Antiguamente las llamábamos Metodologías Waterfall (en cascada), que eran la forma de trabajo que considerábamos buena.
Nadie puede dudar que no hay opción más eficiente que una metodología WATERFALL.
El problema es que es imposible aplicarlas al mundo del software.

  DIA 1: Toma de requisitos (se consideraba PERFECTA e INVARIANTE)
    DIA 2: Diseño del sistema en su conjunto / Planificación del proyecto
       DIA 3: Implementación del sistema
           DIA 4: Pruebas del sistema
              DIA 5: Entrega del sistema

El cliente no veía el sistema hasta pasado 6 meses... 1 años.. 2 años... depende del proyecto...
Pero básicamente el cliente no veía el sistema hasta que estaba terminado.

Y cuando lo veía, pedía 50.000 cambios. NORMAL!
Normal porque la toma de requisitos no había sido buena... ni invariante.
- Con el tiempo aparecían cambios que había que hacer.
- Al ver el sistema, el cliente se daba cuenta que había cosas que no había pensado bien.
- Con las mismas, yo, que soy experto en desarrollo, pero no en el negocio, había cosas que no había entendido bien.

**El objetivo de las metodologías ágiles es ir entregando el producto de forma incremental.**

Para qué?  Obtener feedback del cliente mucho más rápido (antes en el tiempo).

Hay más cosas...

---

Lo que mucha gente no explica cuando comienzan en el mundo de las metodologías ágiles es que han resuelto muchos problemas (es verdad)... pero han traído otros tantos encima de la mesa.

ITERACIÓN 1 (SPRINT): **Día 10 de Julio**... R1, R2, R3
Si llegada la fecha (10 de Julio) solo tengo el R1 y R2, qué pasa?
- Suenan alarmas
- Ostias pa'to's la'os
- Se entrega el R1 y el R2
- Y el R3... al siguiente sprint
- PERO LA FECHA NO SE MUEVE NI UN MINUTO !

Si aquí hago paso a producción, eso que implica?
1. Pruebas... prueba a nivel de paso de producción.. pero es más complicao.
   Qué pruebo aquí? R1 y R2 y R3.
2. Instalar... en pre, en pro

ITERACIÓN 2 (SPRINT): **Día 25 de Julio**... R4, R5, R6
1. Qué pruebo aquí? R3, R4, R5, R6.... y el R1 y R2... que he tocao código... y he podido joder algo!
2. Instalar... en pre, en pro

ITERACIÓN 3 (SPRINT): **Día 10 de Agosto**... R7, R8, R9
1. Qué pruebo aquí? R7, R8, R9... y el R1, R2, R3, R4, R5, R6... que he tocao código... y he podido joder algo!
2. Instalar... en pre, en pro

PROBLEMAS NUEVOS:
- Las pruebas se reproducen como ratones/cucarachas.
- Las instalaciones se reproducen como ratones/cucarachas.

Y la pregunta es: DE DONDE SALE LA PASTA/TIEMPO/RECURSOS PARA ESA INGENTE CANTIDAD DE NUEVO TRABAJO?
Y la respuesta es: NI HAY GENTE, NI HAY TIEMPO, NI HAY DINERO.

Pero.. el problema es que hay que hacerlo...
A lo cuál solo hay una solución: AUTOMATIZAR.
- Necesitamos automatizar el empaquetado del código.
- Necesitamos automatizar las pruebas.
- Necesitamos automatizar las instalaciones.
- Necesitamos automatizar el paso a producción.
- Todo lo que pueda automatizarse, hay que automatizarlo 
   Pero.. quién dices eso? quién aboga por ello? DEVOPS

Es imposible por DEFINICIÓN adoptar una metodología ágil sin abrazar una cultura DevOps.
NI HAY PASTA, NI HAY TIEMPO, NI HAY RECURSOS PARA HACER TODO LO QUE ME EXIGEN LAS METODOLOGÍAS ÁGILES.
---

HITO 1: Día 10 de Julio... **R1, R2, R3**
Si llegada a esta fecha(10 de Julio) solo tenía el R1 y R2, qué pasaba?
- Suenan alarmas
- Ostias pa'to's la'os
- Replanificación del hito: Nueva fecha del hito: **Día 15 de Julio**... **R1, R2, R3**

HITO 2: Día 25 de Julio... **R4, R5, R6**

HITO 3: Día 10 de Agosto... **R7, R8, R9**

---

DEVOPS:                Son automatizables?
    PLAN                poco
    CODE                digamos que poco
    BUILD               totalmente
    ----------------------------------> Si consigo automatizar hasta este punto? HACER UN DESARROLLO ÁGIL.
    TEST
    - Definición        digamos que poco
    - Ejecución         totalmente (salvo tipos de pruebas muy específicas)
    ----------------------------------> INTEGRACIÓN CONTINUA: (Continuous Integration)
                                        Tener CONTINUAMENTE la última versión de los desarrolladores en un entorno de INTEGRACIÓN sometida a pruebas automáticas.
                                           Producto? Informe de pruebas
                                           Para qué? Entre otras cosas, para saber qué tal va mi proyecto! (ver ***1)
    RELEASE             totalmente
    ----------------------------------> ENTREGA CONTINUA:     (Continuous Delivery)
                                        Ser capaz de CONTINUAMENTE poner en MANOS DE MI CLIENTE la última versión probada.
                                           Producto? Lo resultante?
                                           Tener disponible el software en un sitio accesible por el cliente.
    DEPLOY              totalmente
    ----------------------------------> DESPLIEGUE CONTINUO:   (Continuous Deployment)
                                        Ser capaz de CONTINUAMENTE poner en PRODUCCIÓN la última versión probada.
                                            Producto? Lo resultante?
                                            Tener instalado el software en el entorno de PRODUCCIÓN de mi cliente.
    OPERATE             totalmente
    MONITOR             totalmente
    ----------------------------------> Hemos adoptado una cultura DEVOPS COMPLETA


---
Extraído del manifiesto ágil:

> El software funcionando es la MEDIDA principal de progreso.  ***1

    Esta frase define un indicador para un cuadro de mando

La MEDIDA principal de progreso es "El software funcionando"
Informal.. semántico: La frase la podemos reescribir como:

    La forma en que vamos a medir qué tal va el proyecto es mediante el concepto "Software funcionando".

Formal... análisis sintáctico:

        Núcleo    adj    comp. prep.   Cópula o atributo
    ------ --------- -----------    -------------------------
    La MEDIDA principal de progreso es "El software funcionando"
    ------------------------------- ----------------------------
    SUJETO                               PREDICADO

Que leches es ese concepto "Software funcionando"?
Tampoco es complicado.. software que funciona... que hace lo que se espera de él... sin desviaciones.

Quién dice que el software funciona?
 - ~~EL CLIENTE~~
 - LAS PRUEBAS

---

Eso es el concepto básico de DEVOPS...
A raíz de eso... nos hemos inventado algunas otras palabrotas!

DEVSECOPS:  DevOps + Teniendo en cuenta conceptos de seguridad en cada una de las fases del desarrollo y su ciclo de vida.

MLOPS:... Este nos interesa más.!!!! que estamos en un curso de IA!
Es una extensión de DevOps para el desarrollo de sistemas de IA/Machine Learning.
La idea es que del entorno de producción, podamos extraer datos (lo ideal que de forma automática) para alimentar nuevas versiones de nuestros modelos de IA (lo ideal es que de forma automática).

Los modelos, es muy muy muy poco probable que funcionen a la primera. Un modelo debe ir evolucionando con el tiempo. Y para ello necesita cada vez datos más precisos y actualizados. Lo que intentaremos es capturar datos del entorno de producción para alimentar nuevos versiones de los modelos de IA que estamos usando en esos entornos de producción.

---

Ésto es algo que tendremos que ver en la formación.
No es sólo cuestión de montar un bot que responda preguntas.
Es cuestión también de ir capturando datos de las conversaciones que se producen en el entorno de producción para ir mejorando la bbdd de preguntas y respuestas que alimenta al bot.

---
Lo primero será habilitar la captura de datos de las conversaciones que se producen en el entorno de producción.
Lo segundo será automatizar en lo posible (y no siempre es muy posible.. al menos al 100%) el proceso de preparar esos datos en algo que valga para alimentar una nueva versión del modelo de IA.

---


Cuando montamos un bot, el bot realmente son varias partes:
- Programa que va generando el html (BOT)
- Programa que recibe las peticiones del usuario y las manda al modelo de IA (SERVICIO BOT)
- Modelo de IA que responde a las preguntas del usuario (LANGUAGE MODEL)
  ^^^^ A este modelo es al que interrogamos con la URL de ayer (PREDICTION URL)