# Módulo 8 - Cloud: GitHub Pages (despliegue manual)

App Vite + React + TypeScript desplegada manualmente en GitHub Pages.

## Enlace

- **App desplegada:** https://danivegi.github.io/modulo08-cloud-gh-pages-manual/

## Cómo se despliega

1. `vite.config.ts` usa `base: './'` para que las rutas de los assets sean relativas, ya que GitHub Pages sirve la app en una subcarpeta (`/modulo08-cloud-gh-pages-manual/`) y no en la raíz del dominio.
2. El script `npm run deploy` (definido en `package.json`) hace el build y, con el paquete `gh-pages`, publica el contenido de `dist` en la rama `gh-pages`.
3. GitHub Pages está configurado para servir la rama `gh-pages` (Settings → Pages → Deploy from a branch).

El despliegue es manual: la web solo se actualiza al ejecutar `npm run deploy`.