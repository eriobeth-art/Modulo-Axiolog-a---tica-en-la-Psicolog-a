MÓDULO DE AXIOLOGÍA · V4.7 · CONFIRMACIÓN AUTOMÁTICA

OBJETIVO DEL HOTFIX
La V4.6 sí guardaba la evidencia en Google Sheets, pero algunos navegadores no recibían el mensaje de confirmación devuelto por el iframe de Apps Script. Por eso el alumno veía "El servidor tardó demasiado en responder" aunque su fila ya estuviera registrada.

V4.7 añade una segunda vía independiente de confirmación:
1. El formulario POST sigue enviando toda la evidencia al backend.
2. El frontend consulta automáticamente al backend cada 1.5 segundos mediante JSONP.
3. En cuanto detecta CLIENT_SUBMISSION_ID en Sheets, avanza a la pantalla de resultado sin depender del postMessage del iframe.
4. Si un alumno de V4.5/V4.6 recarga y su evidencia ya estaba guardada, V4.7 la reconoce automáticamente y recupera el resultado.

ORDEN DE ACTUALIZACIÓN
A) GOOGLE APPS SCRIPT
- Reemplazar Code.gs por backend/Code.gs.
- Guardar.
- Implementar > Administrar implementaciones > editar implementación existente > Nueva versión.
- Mantener la misma URL /exec.
- Al abrir la URL /exec debe indicar V4.7 y "Confirmación automática de registros activa".

B) GITHUB PAGES
- Sustituir index.html y config.js con los de frontend/.
- También puede subir 404.html, README.md y SEGURIDAD.md.
- Commit a main.
- Esperar 1-2 minutos y hacer Ctrl+F5.

ALUMNOS ATORADOS
- No borrar caché ni datos del sitio.
- No cambiar de equipo/navegador.
- Después de publicar V4.7, recargar la misma página.
- V4.7 verificará automáticamente si su registro ya existe y, si existe, mostrará su resultado.

BACKEND CONFIGURADO
https://script.google.com/macros/s/AKfycbxWmCLVBpeXUJUlbq0cjKyuT1LSLk62oR08sUW_-tp8a3U5n8ZEtJiw7C8FvU6rEGc/exec
