

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

git add <archivo-olvidado>
git commit --amend

```
### Nota importante
El uso de `--amend` **cambia el historial de commits**, por lo que es recomendable usarlo solo si aún no has hecho `push` de los cambios al repositorio remoto. Si ya subiste el commit, hacer `--amend` puede provocar conflictos para otros colaboradores.

