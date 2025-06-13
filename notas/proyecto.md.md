
Montar un programa python para pruebas automatizadas de mi BBDD preguntas.

La realidad es que microsoft tiene ya un programa de pruebas automatizadas de estos modelos.
Por desgracia es un poco ruinoso!

---

# Montar un bot para preguntas y respuestas de un tema X

Pero no solo montarlo... eso es fácil.. ya lo sabemos hacer!
El problema es montar algo que facilite el ciclo de vida de eso a lo largo del tiempo.

 GIT (estructura de carpetas / archivos)
 Algún mecanismo de pruebas automatizadas (inicialmente podemos usar el del microsoft)
 Montar un Pipeline de CI > Informe de Pruebas (para saber si lo que estamos haciendo funciona o no)
      1º Actualizar la base de preguntas (en desarrollo) con las preguntas que tenemos ahora mismo
      2º Ejecutar las pruebas automatizadas para ver si se responden bien
  ^
  Ésto querremos que se ejecute cuando se solicite un commit a la rama desarrollo
  Y sólo si las pruebas dan OK, se subirá ese commit a desarrollo

 Montar un Pipeline de CD > Entrega continua
    ^
    Obtener unas URLs accesibles que apunten a la última versión aprobada de nuestro juego de preguntas y respuestas

 Montar un Pipeline de CD > Despliegue continuo
    ^
    Cargar las URLs BUENAS 
    Invocar al API de Language Studio para que haga el DEPLOY


---

# Cómo organizamos el proyecto por dentro.. carpetas.. archivos...

Preguntas, con sus respuestas
Pruebas
- Al final, una prueba qué es? PREGUNTA + RESPUESTA ESPERADA.. pero esa repuesta debemos tenerla registrada en el archivo de preguntas y respuestas... la queremos escribir 2 veces? Lo suyo es que no. De hecho.. Al final... una prueba conceptualmente no es sino una alternativa a una pregunta que ya existe ... sin que esa alternativa esté registrada en el archivo de preguntas y respuestas.

Lo suyo sería tener solamente 1 fichero por SUBTEMA... Con sus preguntas, respuestas... y pruebas (que no son sino reformulaciones de la pregunta original).
El problema es que ese fichero NO ES EL FICHERO con el que alimentar al chatbot... sino las alternativas estarían dentro.
Nos hace falta un programita que desde un fichero nuestro de preguntas, respuestas y pruebas genere:
- Un fichero de preguntas y respuestas para alimentar al chatbot
- Un fichero de pruebas automatizadas

Ese programita será mu simple... lo haremos en PYTHON....
Nuestro fichero, el que tiene todo, lo podemos escribir en formato YAML.
Y desde ese fichero generar los ficheros TSV necesarios para alimentar al chatbot y las pruebas automatizadas.

---

Fichero YAML:
```yaml
tema: "Tema X"
preguntas:
  - pregunta: "Pregunta 1"
    respuesta: "Respuesta 1"
    alternativas:
      - "Alternativa 1 Pregunta 1"
      - "Alternativa 2 Pregunta 1"
    subpreguntas:
      - pregunta: "Subpregunta 1.1"
        respuesta: "Respuesta Subpregunta 1.1"
      - pregunta: "Subpregunta 1.2"
        respuesta: "Respuesta Subpregunta 1.2"
    pruebas:
      - pregunta: "Alternativa 1 Pregunta 1"
      - pregunta: "Alternativa 2 Pregunta 1"
```

qnautils.py --fichero "fichero.yaml" --generate-test "fichero-test.tsv" --generate-qna "fichero-qna.tsv" --stats

qnautils.py --directorio --stats
  Subtemas + Preguntas + Respuestas + Alternativas + Subpreguntas + Pruebas

qnautils.pu --ejecutar-pruebas --fichero "fichero.yaml"
qnautils.pu --ejecutar-pruebas --directorio "directorio"
 Y me genere informes consolidados
    Por temas, cuantas van bien, cuantas mal
    Cuales van mal
    Genere unos gráficos:
    - Gráfico tarta por tema: cuantas van bien, cuantas mal
    - Histograma de las confianzas de las respuestas
    - Si tengo respuestas con confianza baja el sistema que estamos montando será FRÁGIL.. a mínimos cambios, todo podría dejar de funcionar.


En el pipeline de CI: TRIGGERS: Se ejecuta cuando alguien solicita que pase un commit a desarrollo
1. Crear un proyecto nuevo en AZURE LANGUAGE STUDIO para el SUBTEMA que competa
    --> LLAMADA HTTP  
2. Cargo el/los ficheros que me digan
    --> LLAMADA HTTP  
3. Ejecuto las pruebas automatizadas
     Mi programa (que internamente hace llamadas HTTP)
5. Genero un informe de pruebas
     Una función de mi programa
6. Borro el proyecto de Language Studio
    --> LLAMADA HTTP  

En pipeline de C.Delivery: Se ejecuta cuando alguien pide que pase un commit a main
1. Generar los archivos de preguntas y respuestas
   - Lo hace nuestro programa 
3. Los dejo cargados en el repositorio de mi proyecto como artefactos
   GITLAB/GITHUB permiten actuar como repositorios de artefactos.
    - Me lo regala github actions... azure devops.. gitlab ci/cd

En el pipeline de C.Deploy: Se ejecuta manualmente
1. Cargo la última versión de los artefactos generados en el pipeline de C.Delivery (Los últimos artefactos-ficheros de QnA)
   en el proyecto BUENO DE VERDAD (el que no borramos de tanto en tanto) 
    --> LLAMADA HTTP
2. SMOKE TEST (es una prueba no exhaustiva para comprobar que el sistema funciona de forma básica)
    ---> Aquí podemos tirar por la calle de en medio... que se hagan las mismas pruebas en este entorno
    Hacer 4 peticiones
    Es la típica que hacemos después de instalar una app.. para ver si se ha instalado bien.
3. DEPLOY del proyecto en Language Studio para su paso a producción
    --> LLAMADA HTTP
4. SMOKE TEST (es una prueba no exhaustiva para comprobar que el sistema funciona de forma básica)
    ---> Aquí podemos tirar por la calle de en medio... que se hagan las mismas pruebas en este entorno
    Hago 4 peticiones.
