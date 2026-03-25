1\)

El comando git rebase -i sirve para abrir un editor con la lista de tus commits recientes para que puedas decider qué hacer con cada uno. Su ventaja, por ejemplo, es legibilidad.



2\)

reword = usar el commit pero cambiar el mensaje (Git abrirá un editor para que cambies, por ejemplo, "añade el motor..." por "Implementa motor de búsqueda con filtros". El código no cambia, solo la etiqueta).

squash = combinar este commit con el anterior (Git unirá el contenido del #2 dentro del #1. Luego te pedirá un nuevo mensaje para ese commit único y al final tu historial ahora es más corto y limpio).

drop = eliminar el commit (en caso de poner drop en lugar de pick el commit desaparece por completo del historial y es como si nunca hubiera existido).



3\)

Usar mal git rebase -i en ramas compartidas es peligroso porque reescribe el historial de commits. Al modificar, combinar o reordenar commits, Git genera nuevos identificadores para ellos, lo que rompe la sincronización con cualquier otra persona que tenga una copia de esa rama.

