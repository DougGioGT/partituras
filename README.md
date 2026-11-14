# AtrilSync Pro

Atril digital para partituras PDF con sincronización en tiempo real entre tablets (Maestro → Músicos).

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `atrilsync`).
2. Sube estos archivos a la raíz del repositorio:
   `index.html`, `sw.js`, `manifest.json`, `icon.svg`, `README.md`
3. Ve a **Settings → Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`. Guarda.
5. Espera 1–2 minutos. Tu app quedará en:
   `https://TU-USUARIO.github.io/atrilsync/`

GitHub Pages usa `https://`, que es lo que necesita la cámara para escanear QR y el modo instalable.

## Instalar en la tablet

1. Abre el enlace una vez **con internet** (así se guarda en caché).
2. Chrome/Android: menú ⋮ → *Instalar app* o *Añadir a pantalla de inicio*.
   Safari/iPad: Compartir → *Añadir a pantalla de inicio*.
3. Carga tus PDFs desde **📂 Cargar PDFs**. Se guardan en el dispositivo y funcionan sin internet.

## Nombres de los PDFs

`Cancion 1 - Trompeta 1.pdf`, `Cancion 1 - Trompeta 2.pdf`, etc.
(Canción, guion, instrumento.)

## Conexión entre tablets

- **Sin internet (QR):** misma red Wi-Fi o hotspot de un celular. El Maestro genera el QR, el músico lo escanea y el Maestro escanea la respuesta. Se repite por cada músico.
- **Por internet (Salas):** el Maestro crea una sala (ej. "Metales") y los músicos la eligen en la lista de salas disponibles. PIN opcional.

## Actualizar la app

Cuando cambies `index.html`, sube también el cambio de versión en `sw.js`
(`const CACHE = 'atrilsync-v3'` → `v4`) para que las tablets descarguen la nueva versión.

## Notas

- Los PDFs no se suben a ningún servidor: quedan en cada tablet.
- El PIN de las salas solo evita entradas accidentales; no es cifrado.
