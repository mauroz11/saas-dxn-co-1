# App DXN Colombia

Archivos listos para publicar en GitHub Pages.

## Acceso SaaS local

La version actual incluye una capa SaaS multi-tenant estatica para prototipo:

- Super Admin: `SUPER-DXN-2026`
- Usuario demo activo: `DXN-DEMO-2026`

El Super Admin entra por el enlace reservado `dxn-svc-7f29c4.html`.
Los usuarios entran por `index.html`.
Los registros nuevos quedan pendientes y se aprueban desde el panel `Super Admin`.
En el registro no se solicita contrasena: el Codigo DXN registrado queda como
Clave de Acceso una vez el usuario sea aprobado.
Los datos del prototipo se guardan en `localStorage`; para produccion se debe migrar
a una base de datos segura con RLS, por ejemplo usando el esquema de
`docs/saas-multitenant-supabase.sql`.

Sube a GitHub todo el contenido de esta carpeta, incluyendo:

- `index.html`
- `dxn-svc-7f29c4.html`
- `assets`
- todos los archivos `.pdf`, `.png`, `.txt` y `.js` que estan junto al `index.html`

No subas solo el `index.html`, porque la app necesita la carpeta `assets` para cargar las imagenes.
