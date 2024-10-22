# Objetivos

Crear un repositorio en GitHub donde cada miembro del grupo documente un comando di Git, explicando su propósito y ejemplos.

## Introducciones

1. **Crear el repositorio**:
    Crear un nuevo repositorio en GitHub y agrega a tus compañeros como colaboradores.
2. **Crear Ramas**:
    Cada colaborador debe crear una rama con su nombre:
    `git checkout -b nombre_del_colaborador`
3. **Documentar Comandos**:
    Cada miembro documentará un comando específico de Git en un archivo `nombre_comando.md` en la raíz del repositorio.

    Ejemplo de contenido para `add.md`:

    ```md
    ## Comando: git add
    **Propósito**: Añadir cambios al área de preparación.

    **Ejemplo**:
    ```bash
    git add archivo.txt

    ```

    ```

4. **Subir Cambios**:
    Agregar, commitea y sube tu archivo:

    ```bash
    git add nombre_comando.md
    git commit -m "Agregar documentación para [nombre del comando]"
    git push origin nombre_del_colaborador
    ```

5. **Crear un Pull Request**:
    Crear un `Pull Request` para fusionar tu rama con la rama `main`.

6. **Marge con la Rama Principal**:
    Revisa y acepta los `Pull Request`para fusionar los cambios en `main`.

## Resultado Esperado

Un archivo `comandos.md` que contenga documentación clara sobre varios comandos de Git, incluyendo su propósito y ejemplos.

