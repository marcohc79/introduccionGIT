\[[Init](#init)\] - \[[Add](#add)\] - \[[Commit](#commit)\] - \[[Push](#push)\] - \[[Log](#log)\] - \[[Branch](#branch)\] - \[[Checkout](#checkout)\] - \[[Git Status](#git-status)\] - \[[Merge](#merge)\] - \[[Clone](#clone)\] - \[[Pull](#pull)\]

---

# Init
El comando `git init` se utiliza para **inicializar un nuevo repositorio de Git** en el directorio actual. Es el primer paso para empezar a rastrear archivos en un proyecto con Git, y convierte el directorio en un repositorio donde se puede llevar un historial de cambios.

Cuando ejecutas `git init`, Git crea un subdirectorio oculto llamado `.git`, que contiene todos los archivos necesarios para gestionar la historia y la configuración del repositorio. Después de este paso, puedes añadir archivos al área de preparación y comenzar a realizar commits para construir el historial de cambios.

**Ejemplo**:
```bash

git  init

```
# Add
El comando `git add` se utiliza para **añadir archivos al área de preparación (staging area)** en Git. Esto significa que Git comenzará a rastrear los cambios de estos archivos, preparándolos para ser confirmados (commiteados) en el historial del repositorio.

El área de preparación es una etapa intermedia: los archivos que se encuentran en esta área aún no se han registrado en el historial de Git, pero están listos para ser confirmados. Esto te permite seleccionar específicamente los cambios que deseas incluir en el próximo commit.

**Ejemplo**:
* Archivo especifico:
```bash

git  add [archivo]

```
Esto añadira el archivo especifico en el staging area.
* Agregar todos los archivos modificados:
```bash

git add .

```

# Commit
El comando `git commit` se utiliza para **confirmar los cambios** que están en el área de preparación (staging area) y registrarlos en el historial de Git. Al hacer un commit, se crea un "punto de control" en el historial del repositorio, permitiendo que puedas volver a esta versión del proyecto en el futuro si es necesario.

Cada commit en Git tiene un mensaje de confirmación que describe los cambios realizados, lo cual es importante para llevar un registro claro y útil del historial del proyecto.

**Ejemplo**:
```bash

git commit -m "mensaje descriptivo del commit"

```
 La opción `-m` permite especificar un mensaje de confirmación directamente en la línea de comando, lo cual es obligatorio para describir qué cambios se han hecho.

**Otros usos de ejemplo**:
Realizar un commit de los cambios con un mensaje multi-línea:
```bash

git commit

```
Sin el `-m`, Git abrirá el editor de texto predeterminado, permitiéndote escribir un mensaje de varias líneas.

Modificar el último commit (mensaje o archivos):
```bash

git commit --amend -m "Nuevo mensaje para el último commit"

```
La opción `--amend` en el comando `git commit` se utiliza para **modificar el último commit** que se realizó en el repositorio, permitiéndote cambiar el mensaje o añadir archivos adicionales al commit.
**Añadir archivos adicionales**: Si te olvidaste de añadir algún archivo en el último commit, puedes hacerlo en dos pasos:

-   Primero, usa `git add` para añadir el archivo faltante al área de preparación.
-   Luego, usa `git commit --amend` para agregar ese archivo al commit existente, en lugar de crear un commit nuevo.

```bash

git add [archivo-olvidado]
git commit --amend

```
### Nota importante
El uso de `--amend` **cambia el historial de commits**, por lo que es recomendable usarlo solo si aún no has hecho `push` de los cambios al repositorio remoto. Si ya subiste el commit, hacer `--amend` puede provocar conflictos para otros colaboradores.

# Push
El comando `git push` **sube los commits locales al repositorio remoto**. En otras palabras, envía todos los cambios confirmados (commits) en tu rama local al servidor remoto, permitiendo que otros colaboradores puedan ver y trabajar con esos cambios.
**Ejemplo**:

```bash

git push [nombre-remoto] [nombre-rama]

```
-   **`[nombre-remoto]`**: Generalmente, el repositorio remoto se llama `origin` (nombre predeterminado al clonar o agregar el remoto), aunque podrías darle otro nombre.
-   **`[nombre-rama]`**: Especifica la rama a la que quieres hacer push, como `main`, `master`, `develop`, etc.

*Este comando sube los commits de la rama `main` al repositorio remoto `origin`.*
**Una vez que has confirmado todos los cambios en tu repositorio local y estás listo para compartirlos en el remoto**. Esto es necesario en un entorno colaborativo, donde otros colaboradores también pueden descargar (`pull`) y ver tus actualizaciones.


# Log
Muestra el **historial de commits** del repositorio. Puedes ver la secuencia de commits realizados, incluyendo autor, fecha y mensaje de cada commit.

**Ejemplo:**
```bash

git log

```

# Branch
Permite **ver, crear o eliminar ramas** en el repositorio. Este comando es útil para gestionar diferentes versiones del proyecto sin afectar la rama principal.
**Listar todas las ramas ejemplo:**
```bash

git branch

```
**Crear una nueva rama ejemplo:**
```bash

git branch [nombre-rama]

```
**Eliminar una rama ejemplo:**
```bash

git branch -d [nombre-rama]

```
# Checkout
Se usa para **cambiar de rama** o restaurar archivos en el área de trabajo.

**Cambiar a una rama específica ejemplo:**
```bash

git checkout [nombre-rama]

```
**Crear y cambiar a una nueva rama al mismo tiempo ejemplo:**
```bash

git checkout -b [nombre-rama]

```
**Restaurar un archivo modificado al último commit ejemplo:**
```bash

git checkout -- [archivo]

```
# Git Status
El comando **git status** es un comando relativamente sencillo que muestra el estado del *directorio de trabajo* y del *área de preparación (staging area)*. 
Permite ver que archivos modificados se han añadido al *área de preparación*, cuáles no han sido añadidos, y qué archivos no están siendo rastreados en el repositorio. Además, proporciona algunos consejos básicos sobre cómo mover archivos entre estas etapas.
Acá un pequeño ejemplo:
Este seria el comando: 

    git status
en la consola se vería de esta manera:
![Ejemplo|center](https://www.aluracursos.com/blog/assets/iniciando-repo-con-git/imagen6.png)

# Merge
Combina los cambios de una rama específica con la rama en la que estás trabajando actualmente. Es útil para **fusionar cambios** después de completar una nueva característica.

**Ejemplo:**
```bash

git merge [nombre-rama]

```
# Clone
Clona un repositorio remoto, creando una copia completa en tu máquina local. Es el primer paso para obtener una copia de un proyecto que ya existe en GitHub u otro servidor Git.
```bash

git clone [URL-repositorio]

```
# Pull


  

El comando `pull` es comúnmente utilizado para actualizar el repositorio local con los cambios realizados en el repositorio remoto.

Específicamente, realiza dos acciones principales:

  

1.  **Fetch**: Descarga las actualizaciones desde el repositorio remoto hacia el repositorio local. Esto incluye obtener

las ramas, etiquetas y otros objetos desde el repositorio remoto, sin hacer camios en el área de trabajo.

  

2.  **Merge**: Fusiona los cambios descargados en la rama actual en la que estás trabajando. Es decir, incorpora las

nuevas confirmaciones (`commits`) del repositorio remoto a tu rama local. Si los cambios entre la rama local y la remota son compatibles, Git realizará una fusión automática. Sin embargo, si hay conflictos (por ejemplo, si tanto la versión local como la remota modificaron la misma parte de un archivo), se requerirá que resuelvas estos conflictos manualmente.

  

### Sintaxis

  

```bash

git  pull [opciones] [repositorio] [rama]

```

  

**Ejemplo**:

  

```bash

git  pull  origin  main

```