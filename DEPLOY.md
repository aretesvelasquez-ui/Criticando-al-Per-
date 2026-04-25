# Despliegue público de la app

Esta configuración permite desplegar el frontend de React en Netlify y obtener un enlace público.

## Qué incluye
- `netlify.toml`: configura la carpeta base del frontend y el comando de build
- `app/app/backend/app/frontend/app/frontend/.env`: define la URL pública del backend para React

## Pasos para desplegar
1. Sube este repositorio a GitHub o GitLab.
2. Crea un sitio en Netlify y conéctalo al repositorio.
3. Netlify usará `netlify.toml` automáticamente:
   - carpeta base: `app/app/backend/app/frontend/app/frontend`
   - comando: `yarn build`
4. Al finalizar el despliegue, Netlify te dará un enlace público tipo `https://<tu-sitio>.netlify.app`.

## Notas importantes
- El frontend consumirá el backend definido en `REACT_APP_BACKEND_URL`.
- Si tu backend no está público, primero debes desplegarlo en un servicio como Render, Railway o Fly.io y luego actualizar esta URL.
- Si cambias el backend, actualiza la URL en `netlify.toml` y en `app/app/backend/app/frontend/app/frontend/.env`.
