
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

