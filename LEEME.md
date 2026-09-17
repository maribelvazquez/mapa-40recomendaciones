# Mapa de las 40 Recomendaciones del GAFI

App de estudio de 360Educa (GMC360) para Reto 40 · Certificación CNBV PLD/FT.
Ruta: Transversales. Armada el 16/09/2026.

Fuente: FATF (2012-2026), International Standards on Combating Money Laundering and the Financing of Terrorism &amp; Proliferation · The FATF Recommendations, adoptadas por el Pleno en febrero de 2012 y actualizadas a junio de 2026. Resumen y traducción didáctica de 360Educa.

## Qué hay en esta carpeta

- `index.html` — la app completa: mapa mental, Modo recitar, trampas, cifras y simulador con los reactivos. Al terminar una ronda o simulacro, el alumno puede imprimir o guardar en PDF su resultado y las preguntas que falló, con la respuesta y su fundamento. No necesita ningún otro archivo, base de datos ni clave de API; funciona en cualquier navegador.
- `LEEME.md` — este archivo.

Secciones de la app: Las 40, La cadena DDC, ¿Recomendación o Nota?, Parejas que confunden, Umbrales, Practicar ▸.

Banco de reactivos: 98 de opción múltiple (4 opciones), verificados contra el texto oficial:
  - El país: riesgos, delitos y sanciones (R.1–8): 26
  - Conocer al cliente (R.9–16): 26
  - Controlar, reportar y beneficiario final (R.17–25): 24
  - Autoridades y cooperación (R.26–40): 22

## Cómo publicarla

**Netlify, sin GitHub:** entra a app.netlify.com/drop y arrastra la carpeta que contiene `index.html`.

**GitHub + Netlify:**
1. Crea un repositorio (sugerido: `mapa-40-recomendaciones-gafi`) y sube `index.html` a la raíz.
2. En Netlify: Add new site → Import from GitHub → elige el repositorio. Deja vacíos «Build command» y «Publish directory».
3. Cada vez que se reemplace `index.html` en el repositorio, Netlify publica la versión nueva sola.

## Cómo corregirla o actualizarla

- **No se edita `index.html` a mano.** Se arma a partir de:
  - la plantilla «Plantilla Mapa Interactivo 360Educa» (artifact en la cuenta de Claude de Maribel Vázquez; respaldo en Drive → 2. ACADEMIA 2026 / 00. METODO Y PLANTILLAS);
  - un archivo de datos (`datos.json`), guardado en el proyecto de Claude del curso.
- **Para cambiar un texto, un reactivo o los colores:** en Claude, con la skill **mapa-norma-360educa**, se corrige el `datos.json` y se vuelve a armar con `construir_app.py`.
- **Si cambia la norma** (reforma), hay que revisar el mapa y el banco contra el texto nuevo antes de volver a publicar.

## Aviso

Material didáctico: los textos están resumidos y no sustituyen la publicación oficial ni son asesoría para un caso concreto.
Progreso de los alumnos: el simulador lo guarda sólo en su propio navegador (clave `gafi40`); no se envía a ningún servidor.
