// Comando para iniciar un nuevo repositorio.
git init

//  Comando para añadir archivos al área de preparación (staging area).
git add

// Comando para confirmar los cambios añadidos al área de preparación.
git commit -m "mensaje"

# Pull

El comando `pull` es comúnmente utilizado para actualizar el repositorio local con los cambios realizados en el repositorio remoto.
Específicamente, realiza dos acciones principales:

1. **Fetch**: Descarga las actualizaciones desde el repositorio remoto hacia el repositorio local. Esto incluye obtener
   las ramas, etiquetas y otros objetos desde el repositorio remoto, sin hacer camios en el área de trabajo.

2. **Merge**: Fusiona los cambios descargados en la rama actual en la que estás trabajando. Es decir, incorpora las
   nuevas confirmaciones (`commits`) del repositorio remoto a tu rama local. Si los cambios entre la rama local y la remota son compatibles, Git realizará una fusión automática. Sin embargo, si hay conflictos (por ejemplo, si tanto la versión local como la remota modificaron la misma parte de un archivo), se requerirá que resuelvas estos conflictos manualmente.

### Sintaxis

```bash
git pull [opciones] [repositorio] [rama]
```

**Ejemplo**:

```bash
git pull origin main
```
