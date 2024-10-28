## USO DE BRANCH

**Opciones genéricas**

-v, --[no-]verbose    mostrar hash y tema, dar dos veces para rama upstream

-q, --[no-]quiet      suprimir mensajes informativos

-t, --[no-]track[=(direct|inherit)]

**Configurar rastreo de rama**

-u, --[no-]set-upstream-to <upstream>

**Cambiar info de upstream**

--[no-]unset-upstream desconfigurar la info de upstream
--[no-]color[=<cuando>]

**usar salida con colores**

-r, --remotes         actuar en ramas de rastreo remoto
--contains <confirmar>

**mostrar solo ramas que contengan el commit**

--no-contains <confirmar>

**mostrar solo ramas que no contengan el commit**

--[no-]abbrev[=<n>]   usar <n> cifras para mostrar los nombres de los objetos

## **Acciones específicas de git-branch:**
-a, --all             listar ramas de remote-tracking y locales

-d, --[no-]delete     borrar ramas totalmente fusionadas

-D                    borrar rama (incluso si no está fusionada)

-m, --[no-]move       mover/renombrar una rama y su reflog

-M                    mover/renombrar una rama, incluso si el destino existe

--[no-]omit-empty     do not output a newline after empty formatted refs

-c, --[no-]copy       copiar una rama y su reflog

-C                    copiar una rama, incluso si el destino existe

-l, --[no-]list       listar nombres de ramas

--[no-]show-current   mostrar el nombre de branch actual

--[no-]create-reflog  crear el reflog de la rama

--[no-]edit-description

**Editar la descripción de la rama**

-f, --[no-]force      forzar la creación, movimiento/renombramiento, eliminación

--merged <confirmar>  mostrar solo ramas que hayan sido fusionadas

--no-merged <confirmar>

**Mostrar solo ramas que no han sido fusionadas**

--[no-]column[=<estilo>]
**Mostrar las ramas en columnas**

--[no-]sort <clave>   nombre del campo por el cuál ordenar
--[no-]points-at <objeto>
**imprimir solo las ramas del objeto**
-i, --[no-]ignore-case
**ordenamiento y filtración son case-insensitive**
--[no-]recurse-submodules
**recurrir a través de submódulos**
--[no-]format <formato>
**formato para usar para el output**