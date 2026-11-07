Nombres: JUAN JOSE HENAO | JULIAN GIRALDO
Usuarios: juanjoseh99 | julian-gc

## Preguntas y respuestas:

### ¿Qué eventos configuraste para disparar tu workflow y por qué?
Dentro del yaml se configuró para que se ejecute las acciones cada que se hace un push a la rama principal, y además, con el comando workflow_dispatch nos permite ejecutar de manera manual también desde la interfaz de github.

### ¿Qué sistema operativo utiliza el runner ubuntu-latest y por qué puede ejecutar tu workflow aunque tu computadora sea Windows o macOS? ¿Qué relación tiene el runner con el shell de los pasos run?
Utiliza el sistema operativo de Linux. El flujo se ejecuta sobre una máquina virtual de github.

### Menciona al menos 3 acciones pre-construidas del Marketplace de GitHub Actions no mencionadas en este material. Excluye actions/checkout, actions/setup-python, actions/upload-artifact y aws-actions/configure-aws-credentials, aunque alguna solo aparezca como ejemplo conceptual. Describe qué hacen y para qué sirven.
- *actions/cache:* Guarda dependencias (pip, npm, etc.) entre ejecuciones y las restaura. Acelera los workflows y ahorra minutos.
- *actions/download-artifact:* Descarga artefactos generados por otro job o ejecución. Sirve para pasar archivos entre jobs.
- *actions/labeler:* Asigna etiquetas automáticamente a los pull requests según los archivos que modifican. Organiza las revisiones.

### ¿Qué es un secreto en GitHub Actions y para qué se usa? ¿Cómo lo usarías en tu workflow?
Un secreto es una variable cifrada que se guarda en GitHub, en el repositorio, el entorno o la organización. Sirve para almacenar información sensible que no debe aparecer en el código ni en el historial de Git

### Reflexiona sobre el uso de GitHub Actions en tu flujo de trabajo diario. ¿Qué tareas automatizarías? ¿Por qué?
Juan José:
GitHub Actions lo veo muy útil, más que todo para la ejecución de ETL, ya que frecuentemente debo ejecutar procesos de extracción y procesamiento de información que muchas veces necesitan de mi monitoreo y dependen de una máquina encendida. Podría programar las ejecuciones para que corran en un horario específico o hacerlo a partir de un trigger, en el que se ejecute cada vez que envían un correo o se manda un documento a una carpeta.

### Reflexiona sobre el uso de GitHub Actions en tu flujo de trabajo diario. ¿Qué tareas automatizarías? ¿Por qué?
Julián:
En mi trabajo diario vería GitHub Actions menos como un programador de tareas y más como un control de calidad automático. Lo usaría para revisar mis scripts SQL con un linter cada vez que hago un cambio y para ejecutar pruebas de calidad de datos (duplicados, nulos, totales que no cuadran) que me alerten antes de que un error llegue al dashboard.


## Ejecución exitosa del workflow
Run python mi_script.py
Autor: JUAN JOSE HENAO | JULIAN GIRALDO
Sistema Operativo: Linux 7.0.0-1019-azure
Fecha y hora desde Python: 2026-11-07 14:41:18.691118

https://github.com/Juanjoseh99/entregable-1-cicd/actions/runs/42382756703/job/128433662303
