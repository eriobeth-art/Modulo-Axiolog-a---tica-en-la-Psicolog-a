# Módulo de Axiología · UAEMéx · V4.6 HOTFIX
## Paquete para GitHub Pages

Este paquete es la parte pública del módulo. Está preparado para GitHub Pages y NO contiene la clave docente.

## Archivos que se suben a GitHub

- `index.html`
- `config.js`
- `.nojekyll`
- `404.html`
- `README.md`
- `SEGURIDAD.md`

## Antes de publicar

Primero implementa el paquete separado de Google Apps Script como aplicación web.

Después copia la URL que termina en `/exec` y abre `config.js`.

Sustituye:

```js
BACKEND_URL: "PASTE_APPS_SCRIPT_EXEC_URL_HERE"
```

por:

```js
BACKEND_URL: "https://script.google.com/macros/s/XXXXXXXX/exec"
```

## Publicar en GitHub Pages

1. Crea un repositorio nuevo.
2. Sube únicamente los archivos de este paquete.
3. En GitHub abre `Settings > Pages`.
4. En `Build and deployment` selecciona `Deploy from a branch`.
5. Selecciona rama `main` y carpeta `/(root)`.
6. Guarda.
7. Espera a que GitHub muestre la URL pública.

## Funciones conservadas

- identidad institucional UAEMéx;
- actividades de Axiología;
- evaluación sobre 100 puntos;
- guardado local de avance;
- aceptación explícita del modo supervisado;
- supervisión solo después de aceptar la casilla;
- primera incidencia: advertencia;
- segunda incidencia: bloqueo;
- desbloqueo validado por Apps Script;
- registro en Google Sheets;
- acuse PDF en Google Drive;
- descarga del acuse por el alumno;
- retroalimentación según calificación.

## Importante

La calificación y la clave docente se validan del lado del servidor. Las respuestas correctas no se incluyen en `config.js`.


## Backend configurado

Este paquete ya está vinculado al endpoint publicado de Google Apps Script:

`https://script.google.com/macros/s/AKfycbyz_cyROYZgCRvjjLdbwdv5QdASar6x8eEcPIGkzQ/exec`

La URL con terminación `/dev` es para pruebas dentro del editor.  
Para GitHub Pages y estudiantes se utiliza `/exec`.


## Rescate de la V4.5

La V4.6 mantiene deliberadamente la clave local `axiologia_github_v4_5` para recuperar el avance guardado de estudiantes que recarguen la página durante la contingencia. No cambies esa clave hasta terminar el grupo actual.
