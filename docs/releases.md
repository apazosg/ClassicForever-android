# Versiones y notas de publicación

La numeración propia de ClassicForever Android comienza en **0.0.1**, independientemente de las versiones de los proyectos en los que se basa.

## Numeración

- **0.0.2, 0.0.3…:** correcciones y ajustes menores.
- **0.1.0, 0.2.0…:** nuevas funciones o mejoras relevantes.
- **1.0.0:** primera versión que decidamos considerar estable.

Cada publicación usa estos nombres, sustituyendo la versión correspondiente:

- Versión en la aplicación: `0.0.1`.
- Tag: `v0.0.1`.
- Título: `ClassicForever Android 0.0.1`.
- Archivo: `ClassicForever-Android-0.0.1.apk`.

Las releases se publican como publicaciones normales de GitHub. Que la versión empiece por `0` no requiere marcarla como *prerelease*: las limitaciones experimentales se explican en sus notas. Los avisos de la aplicación consultan la última release publicada, no las marcadas como *prerelease*.

## Notas de cada release

Las notas se escriben en español, con cambios funcionales comprensibles para quien utiliza la aplicación. No incluyen listas de commits ni detalles internos de programación. Se omiten los apartados vacíos y solo se describen funciones o resultados comprobados.

La primera release presenta las funciones disponibles, en lugar de compararse con una publicación anterior que no existe. Las siguientes explican los cambios respecto a la versión pública anterior.

La aplicación muestra las mismas notas publicadas en GitHub; no se mantiene otro changelog separado.

```markdown
Breve resumen de lo más importante de esta versión.

## Novedades
- Ahora puedes…

## Mejoras
- Resulta más sencillo…

## Correcciones
- Corregido un problema que impedía…

## Limitaciones conocidas
- Problemas relevantes que siguen pendientes.

## Instalación
Descarga e instala el APK adjunto.
[Indicaciones especiales, solo cuando sean necesarias.]
```

## Publicar una versión

1. Asignar la versión visible y aumentar el contador interno de Android, manteniendo el identificador y la firma de la aplicación.
2. Preparar las notas funcionales con el formato anterior.
3. Generar y comprobar el APK firmado.
4. Publicar el tag, las notas y el APK en este repositorio.
5. Comprobar la detección desde una versión anterior y la lectura de las mismas notas dentro de la aplicación.

La primera instalación de `0.0.1` sobre las compilaciones anteriores se realiza manualmente, porque esas compilaciones consultan el repositorio anterior. A partir de `0.0.1`, la aplicación consulta las releases de este repositorio.
