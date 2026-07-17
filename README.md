# 50 Labs — Website

Web comercial de **50 Labs**, agencia de agentes de IA y automatizaciones para empresas. Sitio estático de un solo fichero (`index.html`), bilingüe **ES/EN**, sin build step ni dependencias (solo Google Fonts).

## Contenido

- `index.html` — todo el sitio: HTML + CSS + JS + diccionario de textos embebido
- `content.json` — fuente de los textos (ES/EN); el diccionario embebido en `index.html` debe mantenerse sincronizado con este fichero

## Características

- **Diseño "Ledger Light"**: papel cálido/tinta/siena, tipografía Sora + IBM Plex Mono, robots SVG originales y logos reales de herramientas
- **i18n**: español por defecto, toggle EN/ES persistente (`localStorage`), `?lang=es|en` para forzar idioma
- **Formulario de contacto**: envía a `ralcaraz.canals@gmail.com` vía [FormSubmit](https://formsubmit.co) (AJAX, honeypot anti-spam, validación cliente)
  - ⚠️ **Activación pendiente**: el primer envío real dispara un email de confirmación de FormSubmit a esa dirección — hay que hacer clic una vez para activar el buzón
- Secciones: hero (datos y decisiones), demo del briefing, antes/después, 8 sistemas/agentes (Alba y Radar primero), método, integraciones, casos reales, FAQ, CTA, quién está detrás, contacto + legal.html
- Casos: el del fondo de inversión es real (confidencial); "Comercial Atlas, S.L." es una empresa de demostración con datos sintéticos, señalada como tal. Regla del sitio: ningún dato inventado

## Ejecutar en local

```bash
python3 -m http.server 5095
# → http://localhost:5095
```

Al ser una sola página con anclas, no necesita fallback SPA. Desplegable en cualquier hosting estático (GitHub Pages, Vercel, Dokploy/nginx).
