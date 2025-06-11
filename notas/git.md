

GIT: Sistema de control de versión. Sistema de control de código fuente.

COMMIT: Es un cambio en el código subido a un repositorio.
ESO ESTA MAL. Tenemos esta idea de Sistemas de Control de versiones ANTIGUOS: CSV, Subversión.
En esos sistemas, un commit era un paquete de cambios que se subía al repositorio.

En GIT un commit es una foto completa del proyecto en un momento del tiempo...
Como si hiciera botón derecho en la carpeta del proyecto y diera a meter en un zip... TODA LA CARPETA.

Un repositorio es una secuencia de commits.
Cada commit, menos el primero, tiene un Commit padre. Van en secuencia.
Esto es casi cierto... falta un detalle.

Si al final, un repositorio de git fuera una secuencia de copias de seguridad completas del proyecto, en que se diferenciaría GIT de un sistema de backups? LA RAMAS
En los sistemas de backup no hay ramas. En GIT sí.

Un repositorio es un conjunto de ramas... que acumulan secuencias de commits.
Una rama es una linea de evolución temporal del proyecto, paralela a otras lineas de evolución temporal.

-------------------C1-> C2 -> C3 -> C6 -> C7 -> C8 (= C7 + (C5-C7))
                         \                  /
                          ---C2 -> C4 -> C5

Hay una rama que tenemos siempre:
- master/main /antiguamente trunk: NUNCA PUEDO HACER UN COMMIT EN ESTA RAMA, bajo pena de que me corten als uñas muy cortas y me metan la mano en un vaso con zumo de limón!!! Solo puedo llevar a esta rama cosas de otras ramas.
  Todo lo que hay en esta rama se considera APTO PARA PRODUCCIÓN.