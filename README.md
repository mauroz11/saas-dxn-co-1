# App DXN Colombia

Archivos listos para publicar en GitHub Pages.

## Acceso SaaS

La app incluye una capa SaaS multi-tenant con dos modos:

- Supabase: usuarios, organizaciones, sesiones, activacion y suspension reales.
- Local: respaldo con `localStorage` cuando Supabase no esta configurado.

Para activar Supabase:

1. Ejecuta `docs/saas-multitenant-supabase.sql` en Supabase SQL Editor.
2. Edita `assets/supabase-config.js` con tu Project URL y anon public key.
3. Publica la carpeta completa.

Guia completa: `docs/supabase-setup.md`.

Clave inicial administrativa:

- Super Admin: `SUPER-DXN-2026`

El Super Admin entra por el enlace reservado `dxn-svc-7f29c4.html`.
Los usuarios entran por `index.html`.
Los registros nuevos quedan pendientes y se aprueban desde el panel `Super Admin`.
Cuando Supabase esta configurado, la activacion/desactivacion ocurre en la base de datos.
Cuando `assets/supabase-config.js` esta vacio, la app usa modo local sin usuarios de prueba.

El envio de correo al activar usuarios se maneja con la Edge Function
`supabase/functions/send-activation-email` y la tabla `email_events`.

Sube a GitHub todo el contenido de esta carpeta, incluyendo:

- `index.html`
- `dxn-svc-7f29c4.html`
- `assets`
- todos los archivos `.pdf`, `.png`, `.txt` y `.js` que estan junto al `index.html`

No subas solo el `index.html`, porque la app necesita la carpeta `assets` para cargar las imagenes.
