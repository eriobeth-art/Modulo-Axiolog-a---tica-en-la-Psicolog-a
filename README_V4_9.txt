AXIOLOGÍA UAEMéx · V4.9 · FRONTEND GITHUB

CORRECCIÓN PRINCIPAL
- El bloqueo se conserva: primera incidencia = advertencia; segunda = bloqueo.
- El desbloqueo ya NO depende del iframe/postMessage.
- La clave se valida mediante JSONP/GET contra Apps Script.
- Si el servidor tarda, a los 20 s el botón se reactiva y el alumno puede reintentar sin recargar.
- Mientras la actividad está bloqueada o se valida la clave, no se acumulan incidencias espurias por foco.

PUBLICACIÓN
1. Sustituir index.html y config.js en GitHub Pages.
2. No borrar el almacenamiento local del alumno.
3. Mantener la URL /exec actual.
