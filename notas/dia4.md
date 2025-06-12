
                               WebChat

 MODELO LENGUAJE (QnA) < BOT < CANAL
                               Frontal
                         Backend
                         C#
                         JS NodeJS


Depende lo que queramos hacer.
- Una cosa es el modelo de lenguaje (LANGUAGE STUDIO < Preguntas y Respuestas)
- Otra cosa es la implementación del bot (C# o JS/NodeJS)
  Al bot le podemos meter mano o no

Tanto el bot, como el modelo tienen su ciclo de vida INDEPENDIENTE.

Los desarrollaremos, los probaremos, los desplegaremos, analizaremos su funcionamiento y logs, y los mejoraremos de forma independiente.

Para el ciclo de vida del modelo de lenguaje, nos conviene intentar automatizar todo lo que pueda (DEVOPS).
En este caso, que estamos creando un modelo de IA, nos puede interesar incluso: 
- automatizar el proceso de captura de datos del entorno de producción, 
- Con revisión previa.
- para que esos datos alimenten nuevas versiones del modelo de lenguaje.
De esto es de lo que hablaba MLOPS.

---

Ayer decíamos que las preguntas y respuestas son el "CODIGO" de mi modelo de lenguaje.
Es lo único donde meto mano.
El resto me lo dan ellos (AZURE/Language Studio).
No todo el código es IMPERATIVO (IF, FOR, WHILE, SWITCH, etc).

No nos gusta mucho que la fuente de verdad de nuestro modelo de lenguaje (PREGUNTAS Y RESPUESTAS) esté en un sitio que no controlemos. Y el repositorio interno de Language Studio no lo controlamos.
Ese repositorio además no tenemos control de versiones.

---

Imaginad que subo preguntas y respuestas de un producto que vendo.
Y en la web he cargado una versión nueva del producto.
Necesito cargar nuevas preguntas y respuestas asociadas a esa nueva versión del producto.

A ver si para un producto concreto, mi bot está respondiendo a preguntas con respuestas de la versión anterior.

---

Necesitamos esas preguntas en un repositorio de código que controlemos.
Donde pueda ir generando nuevas versiones de preguntas y respuestas.
Y pueda cargarlas de forma sencilla en Language Studio.
Lo mejor, mediante una URL... que apunte a una versión concreta de preguntas y respuestas... o a la última.
Y desde language studio, poder ir actualizando mi base de preguntas y respuestas con esa(s) URL(s).

---

# GIT

REPOSITORIO
    RAMAS                      Lineas de evolución temporal del proyecto.
                               Puedo tener varias líneas de evolución(ramas) en paralelo de mi proyecto
                                en un momento dado del tiempo.
                                Cada commit es una foto completa del proyecto en un momento del tiempo.
        COMMITS                 Foto completa (BACKUPS COMPLETO) del proyecto en un momento del tiempo.
                                Va en secuencia temporal con otros commits.
            ARCHIVOS

## FLUJO DE TRABAJO DE GIT

Esto es lo más importante de GIT. GIT es la fuente de verdad de mi proyecto.
Todo sale de git y todo vuelve a git. Y necesito controlar muy bien los mecanismo por los que ocurre eso.

Un modelo de IA, desde el punto de vista de gestión del código fuente es muy sencillo. Nada que ver con el desarrollo de una aplicación web o de escritorio.

### RAMAS TIPICAS:

Principal (main/master/trunk): 
   - Nunca hacemos commit en esta rama
   - Lo que tenemos en ella se considera APTO PARA PRODUCCIÓN.

Otra rama que tendremos será la rama desarrollo (develop/dev/desa):
   - Aquí es donde hacemos los commits (o no... bueno.. eso en proyectos gordos)
   - Lo que tenemos en esta rama es lo que estamos consolidando para llevar a producción en la siguiente versión (en el siguiente SPRINT).

Pero entonces como llevo las cosas de develop a main? Directamente? NO, ni de coña!
Mediante otra rama que llamaremos RELEASE.
   - En esta rama es donde cerramos un paquete que va a pasar a producción... siempre y cuando se superen las pruebas.


------ main ----------------------C3---------------------------------------------------------------------------->
                                 /  (1) ff (2)
------ release ----------------C3----------------------------------------------------------------------------->
                              /  (1) ff 
------ desa ------CM---CF---CM-------------------------------------------------------------------------------->

(1) merge de tipo fast-forward: Lo que hace es copiar un commit de una rama a otra. No siempre es posible...
    Git solo lo permite si no es destructivo... si hubiese datos que se pierden al hacer ese trabajo, git no lo permite.

(2) qué debe ocurrir para permitir ese ff? Se deben haber superado LAS DE SISTEMA! Las unitarias YA LAS HEMOS DEBIDO DE HABER COMPROBADO ANTES

El caso de los modelos es mucho más sencillo que otro tipo de proyectos de software... ya que:
NO HAY CODIGO COMO TAL... ni decenas de componentes.

- COMPONENTES: MODELO
- CODIGO : PREGUNTAS Y RESPUESTAS (por un tubo... agrupadas en ficheros por producto, por ejemplo)

En este escenario, las pruebas de Integración son iguales a las pruebas de sistema.

Lo normal... es que mi bot responda a preguntas de un tema o de varios? DE VARIOS:
- Háblame de la empresa de tractores
- Háblame del modelo A de tractor
- Háblame del modelo B de tractor
- Háblame del servicio post-venta de tractores

Esas preguntas las diseña una persona o un equipo? Un equipo... no creo que tenga alguien que sea experto en todo.
Cada persona me interesará que tenga su propio archivo de preguntas y respuestas.

Donde lo van subiendo ese archivo a mi repo de GIT? a qué rama? a desa! podría... lo ideal es que no... pero esto ya son DECISIONES!
Que tengo que tomar... desde organización del proyecto. Esto tiene su impacto! ENORME

Si subimos commits en la rama desa... cuando hacemos las pruebas?


Es más.. qué tipo de pruebas vamos a hacer a nuestro sistema (modelo) desde el punto de vista del scope??
- Como poco todo sistema requiere pruebas DE SISTEMA
- Las de integración en este caso me las fumo... o mejor dicho... es que equivalen a las de sistema.... porque no hay muchos más componentes.
- Unitarias? Quiero? Ya vestruz!!!!

Tengo a Menchu... escribiendo preguntas del tractorA:
>Qué potencia tiene el tractor? 1000 cv
Cuando Menchu pruebe sobre su base de de preguntas , ¿Qué potencia tiene el tractor? 1000 cv

Tengo a Felipe... escribiendo preguntas del tractorB:
>¿Qué potencia tiene el tractor? 2000 cv
Cuando Felipe pruebe sobre su base de preguntas, ¿Qué potencia tiene el tractor? 2000 cv

Y cuando junte ambos conjuntos de preguntas, y alguien pregunte, ¿Qué potencia tiene el tractor? ¿Qué pasará? QUE REGADA TIO !!!
UPS! Esta no la habíamos visto venir! Que jodido... y yo aquí a mi bola .. con ms preguntas y eso! y me acabo de meter en un marrón de cojones.


Si Felipe y Menchu están haciendo commits en desa... cuándo se aplican las pruebas unitarias? NPI no hay sitio.. o mejor dicho
El único sitio que hay es cuando subo a release... pero ahí puedo tener ya todo mezclao...
Es más...
Entregamos mañana (Sprint 17).
Y resulta que lo de Menchu no termina de funcionar... y lo de felipe SI.


COMO HABRÍAMOS RESUELTO TODO ESTO:                                                                                      ENTORNOS

------ main ------------------------------------------C6--------------------------------- C11-------------------------> producción
                                                     / ff                                /                                ^ DEPLOY
------ desa ------C0-------------------------------C6--------+--------C9---------------C11------------------------>     test
                   \                    ff - (**1) /          \      / ff        \    / ff : Pruebas sistema+ unitarias
          tractorB-C0------C1------C2------------C6 ----C7 --- \ -- / ------C10 -- C11
           (felipe)  \                                   m.rec. \  / Para esa subida exigimos? Pruebas unitarias + Pruebas sistema
             tractorA-C0 ----C3-------C4----C5--------------C8---C9      y eso lo quiero forzar GITHUB / GITLAB / BITBUCKET !
              (menchu)     según haga commits, irá haciendo sus pruebas unitarias

             una rama como tractorA es lo que llamamos una rama de feature.

    (**1) Pruebas unitarias + Pruebas de Integración = Pruebas de sistema
    C9 = C6 + (C8-C6)
              -------
              patch (se calcula bajo demanda)

En un sistema como este, nos hace falta un entorno de desarrollo / pruebas, entorno de producción.

Menchu y Felipe, van a tener sus propios ficheros cada uno, con sus preguntas y respuestas.
En Azure Language Studio, vamos a configurar URLS de preguntas y respuestas que apunten a los ficheros de preguntas y respuestas de cada uno de ellos (a la última versión)... y de vez en cuando puedo en Language Studio, actualizar las preguntas y respuestas de mi modelo de lenguaje con esas URLS.

Los cambios a mano! Pa otro... Pa los cursos de IA. Ni el subir ficheros!
Esas cosas... para una urgencia... y borrando en cuanto pueda las preguntas después y asegurándome de haberlas llevado al repositorio de git.

Esto no va SOLO como veis de cargar preguntas en una pantalla de Language Studio. Eso es lo de menos.
Esto va de entender como gestiono el ciclo de vida de un modelo de IA, y como lo integro en un flujo de trabajo DEVOPS.
Donde podamos tener un producto de CALIDAD!

- Vais a montar cada uno vuestros propio proyecto.. vuestro propio MODELO DE LENGUAJE DE QnA... con vuestro propio REPO.
- Si queréis os juntáis de 2 en 2... y así jodéis un poco con las ramas.
- Vamos a montar también un programa PYTHON que nos ayude a probar las preguntas: Vamos a necesita rel API REST DE Language Studio.
- Posteriormente intentamos montar un flujo de CI/CD que nos permita llevar a cabo el ciclo de vida del modelo de lenguaje.
  (Esto no da tiempo hoy... lo haremos el lunes a primera hora: ?????)
  Para montar ese proceso de CI/CD tenemos diferentes herramientas:
            Hosting repo     Pipeline de CI/CD
  - Github        √            Github actions / Azure pipelines(Azure DevOps-TFS)
  - Gitlab        √            Gitlab CI/CD   / Azure pipelines(Azure DevOps-TFS) ****

Para el lunes, cuenta de gitlab!

Hoy de momento vamos a montar ese programa en Python que necesitamos!

# Tipos de pruebas

Las pruebas en general, en el mundo del software las clasificamos en base a diferentes taxonomías.
Toda prueba se centra en un aspecto único/concreto de mi sistema.

## En base al objeto de prueba

- P. Funcionales        Se centran en la funcionalidad del software, verificando que cumple con los requisitos funcionales especificados.
- P. No funcionales     Evalúan aspectos no funcionales del software, como rendimiento, usabilidad, seguridad, etc.
    - Pruebas de rendimiento
    - Pruebas de seguridad
    - Pruebas de usabilidad/ux
    - Pruebas de estrés
    - Pruebas de carga

## En base al nivel de prueba (scope)

- P. Unitarias        Cuando me centro en un aspecto único de mi sistema... AISLANDO un componente del resto del sistema.
- P. de integración   Comprueba la COMUNICACIÓN DE 2 COMPONENTES
- P. de sistema       Evalúa el comportamiento del sistema en su conjunto, verificando que todos los componentes funcionan correctamente juntos... y que el sistema se comporta como se espera.

## En base al conocimiento del sistema

- P. de caja blanca   Se centran en la estructura interna del software, verificando el código y la lógica interna.
- P. de caja negra    Se centran en la funcionalidad del software, sin tener en cuenta su estructura interna.

## En base al procedimiento de ejecución
- Pruebas manuales    Se realizan de forma manual, sin automatización.
- Pruebas automatizadas Se realizan mediante scripts o herramientas automatizadas, lo que permite una ejecución más rápida y repetible.

## Otras clasificaciones
- Pruebas de regresión  Una prueba que repito después de hacer un cambio... a ver si he jodido algo que antes funcionaba.
---

# Fabricación de bicicletas

DECATHLON. Fabrico bicis.

    Sillín
    Cuadro
    Ruedas
        Monto la rueda en un bastidor (4 hierros mal soldaos). La instalo y le pego un viaje a ver si gira!
    Manillar
    Sistema de frenos (SHIMANO) Me lo mandan... lo pruebo o lo monto en mis bicis?
        Lo quiero probar... mira que si lo monto y luego trae una tara.. o me encaja bien... y tengo que desmontar 20000 bicicletas la lio parda!
        Donde pongo el sistema de frenos? En una bici? NO
        Monto 4 hierros mal soldaos (un bastidor) y le pongo el sistema de frenos.
        PRUEBA: APRIETO LA PALANCA! y que miro? Miro si la rueda se para? Que rueda? si no tengo rueda.. ni la quiero!
            sistemaFrenos.apretarPalanca();
        Montaré un sensor de presión (algo en lo que confío) entre las pinzas de cierre del sistema de frenos.
        PRUEBA: Aprieto la palanca y miro la presión ejercida por el sistema de frenos sobre el sensor.

    Qué gano: CONFIANZA+1 Vamos bien!

    Empiezo a juntar componentes. Pruebas de INTEGRACIÓN
       Ruedas y el sistema de freno.
       Monto un bastidor (4 hierros mal soldaos) y monto la rueda y el sistema de frenos. Con la rueda en medio de las pinzas de freno.
       PRUEBA: Aprieto la palanca
            sistemaFrenos.apretarPalanca();
            Qué compruebo? Resultado? Que la fuerza ejercida sea mucha o poca? NO ... eso ya lo sé!
        Qué compruebo? Que la rueda se para.
            Y mira que no! Qué ha pasao?
            Pues que las pinzas cierran con mucha fuerza... pero no lo suficiente, como para presionar la rueda.. La rueda es más estrecha de lo que sería necesario para esas pinzas de freno.
            UPS !!!!
            - Tengo un problema en la rueda? NO
            - Tengo un problema en el sistema de frenos? NO
            - Tengo un problema en la comunicación entre la rueda y el sistema de frenos? SÍ

Una vez haga todas las pruebas de integración, paso a probar el sistema en su conjunto.
A ver si el comportamiento es el esperado.. o no.

Me dedico a fabricar TRENES.

    Motor              Me mandan el motor... lo pruebo o lo monto en mis trenes?
    Sistema de freno   Me mandan el sistema de freno... lo pruebo o lo monto en mis trenes?
    Asientos           Me mandan los asientos... los pruebo o los monto en mis trenes?
          Cómo pruebo el asiento? Tengo tren donde instalarlo? NO
          Y si lo tuviera? TAMPOCO

          Pruebas al asiento?
          - UX: Es cómodo o se te queda el culo plano al estar 4 horas sentao!
          - ESTRES: Si tengo el asiento con gente sentándose durante 4 años a 14 horas al día, se rompe? aguante? se desgasta?
          - CARGA:  Si aguanta a una persona de 150kgs...
          - SEGURIDAD: En una curva, al pasajero se le escurre el culo y va pa' los laos? Queda bien anclado?
          Si el asiento lo monto en el vagón y hago esas pruebas... quizás la prueba de SEGURIDAD falle...
          Y no sea porque el asiento es malo... sino porque el vagón en si.. no tiene un buen anclaje al suelo.

          Cuando pruebo el asiento quiero probarlo aislado del resto del resto de componentes.
          Montaré 4 hierros mal soldaos(un chasis) a los que poder fijar mi asiento... 4 hierros que me ofrezcan las garantías mínimas de seguridad.Algo en lo que confíe (4 hierros).
          Esos 4 hierros luego los quiero para algo? NO... pero me hacen falta.                     MOCK 
    Ruedas             Me mandan las ruedas... las pruebo o las monto en mis trenes? 









