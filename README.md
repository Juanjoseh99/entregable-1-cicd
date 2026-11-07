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
- *actions/labeler:*Asigna etiquetas automáticamente a los pull requests según los archivos que modifican. Organiza las revisiones.

### ¿Qué es un secreto en GitHub Actions y para qué se usa? ¿Cómo lo usarías en tu workflow?
Un secreto es una variable cifrada que se guarda en GitHub, en el repositorio, el entorno o la organización. Sirve para almacenar información sensible que no debe aparecer en el código ni en el historial de Git

### Reflexiona sobre el uso de GitHub Actions en tu flujo de trabajo diario. ¿Qué tareas automatizarías? ¿Por qué?
Juan José:
GitHub Actions lo veo muy útil, más que todo para la ejecución de ETL, ya que frecuentemente debo ejecutar procesos de extracción y procesamiento de información que muchas veces necesitan de mi monitoreo y dependen de una máquina encendida. Podría programar las ejecuciones para que corran en un horario específico o hacerlo a partir de un trigger, en el que se ejecute cada vez que envían un correo o se manda un documento a una carpeta.

