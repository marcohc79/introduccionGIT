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

