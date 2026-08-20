# ScoutLab · Sebastián López

Aplicación web de **evaluación, scouting y desarrollo de talento** en fútbol:
8 posiciones · 40 arquetipos · 800 cualidades.

## Qué es

`index.html` es una aplicación de una sola página, totalmente autocontenida:
todo el HTML, CSS, datos y lógica viven en ese archivo. No hay backend, ni
base de datos, ni variables de entorno. Las únicas dependencias externas se
cargan por CDN desde el navegador:

- [Chart.js 4.4.1](https://www.chartjs.org/) — gráficos
- [jsPDF 2.5.1](https://github.com/parallax/jsPDF) — exportación a PDF
- Google Fonts (Space Grotesk, IBM Plex Mono, Inter)

## Uso local

No hace falta compilar nada. Abrí `index.html` en el navegador, o serví la
carpeta con cualquier servidor estático:

```bash
python3 -m http.server 8000
# luego abrir http://localhost:8000
```

## Deploy en Vercel

El proyecto es un sitio estático, sin paso de build.

1. En [vercel.com](https://vercel.com) → **Add New… → Project**.
2. Importá el repositorio `sebastianlopez1660-droid/Scoutlab`.
3. En la configuración del proyecto:
   - **Framework Preset:** `Other`
   - **Build Command:** vacío
   - **Output Directory:** vacío (raíz del repositorio)
   - **Install Command:** vacío
4. **Deploy**. Vercel sirve `index.html` en la raíz del dominio.

Cada push a la rama conectada genera un nuevo deploy automáticamente.

## Estructura

```
index.html    Aplicación completa (HTML + CSS + JS + datos)
vercel.json   Configuración de rutas de Vercel
```
