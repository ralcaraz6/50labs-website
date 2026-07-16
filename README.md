# 50 Labs — Website

Web comercial de **50 Labs**, agencia de agentes de IA y automatizaciones para empresas. Sitio estático de un solo fichero (`index.html`), bilingüe **ES/EN**, sin build step ni dependencias (solo Google Fonts).

## Contenido

- `index.html` — todo el sitio: HTML + CSS + JS + diccionario de textos embebido
- `content.json` — fuente de los textos (ES/EN); el diccionario embebido en `index.html` debe mantenerse sincronizado con este fichero

## Características

- **Diseño "The Ledger"**: crema/tinta/siena, tipografía Fraunces + Source Sans 3 + IBM Plex Mono, estética de imprenta (recibos, sellos, numerales)
- **i18n**: detección de idioma del navegador, toggle EN/ES persistente (`localStorage`), `?lang=es|en` para forzar idioma
- **Formulario de contacto**: envía a `ralcaraz.canals@gmail.com` vía [FormSubmit](https://formsubmit.co) (AJAX, honeypot anti-spam, validación cliente)
  - ⚠️ **Activación pendiente**: el primer envío real dispara un email de confirmación de FormSubmit a esa dirección — hay que hacer clic una vez para activar el buzón
- Secciones: hero, problema (antes/después), 6 agentes, método (4 pasos), integraciones, 3 casos de estudio, precios (3 planes), FAQ, CTA final, contacto
- Los casos de estudio, empresas y métricas son ilustrativos

## Ejecutar en local

```bash
python3 -m http.server 5095
# → http://localhost:5095
```

Al ser una sola página con anclas, no necesita fallback SPA. Desplegable en cualquier hosting estático (GitHub Pages, Vercel, Dokploy/nginx).
