# El Guardián de Chamberí — Instrucciones de la web

## Estructura de carpetas

```
guardian-chamberi/
├── index.html              ← la web completa
├── subir_ionos.py          ← script de despliegue FTP
├── img/
│   ├── portada.jpg         ← portada del libro (del Drive)
│   ├── chamberi-hero.jpg   ← foto grande del fondo del hero
│   ├── chamberi-1.jpg      ← fotos galería (del Drive)
│   ├── chamberi-2.jpg
│   ├── chamberi-3.jpg
│   ├── chamberi-4.jpg
│   ├── chamberi-5.jpg
│   └── autores/
│       ├── christa-stahl.jpg
│       ├── jose-ramon-pardo.jpg
│       ├── nacho-ruiz-hens.jpg
│       ├── nhora-cardenas.jpg
│       ├── santiago-perez-viso.jpg
│       ├── sergio-giraldo.jpg
│       ├── pedro-emilio-ardila.jpg
│       └── primavera-gomez.jpg
```

---

## PASO 1 — Añadir las imágenes

### Fotos de la estación de Chamberí y portada
1. Abre la carpeta de Drive: https://drive.google.com/drive/folders/1L8WMqw20Pzj3BnFDriz7hyrXKPb6Ih4t
2. Descarga las fotos
3. Renómbralas como `chamberi-1.jpg`, `chamberi-2.jpg`... y `portada.jpg`
4. Colócalas en `guardian-chamberi/img/`

### Fotos de los autores
1. Abre la carpeta de Drive: https://drive.google.com/drive/folders/1YM4WCWeBlmcHDLFf47UE9Q38I4yh2-jK
2. Descarga las fotos de cada autor
3. Renómbralas como indica la estructura de arriba
4. Colócalas en `guardian-chamberi/img/autores/`

---

## PASO 2 — Añadir los trailers

1. En Google Drive, haz clic derecho en cada vídeo → Obtener enlace
2. La URL tendrá este formato: `https://drive.google.com/file/d/FILE_ID/view`
3. Copia el FILE_ID (la parte larga en el medio)
4. En `index.html`, busca `TRAILER_ID_1` y `TRAILER_ID_2`
5. Sustitúyelos por los IDs reales

---

## PASO 3 — Configurar el newsletter (Mailchimp, gratis)

1. Crea cuenta en https://mailchimp.com (gratis hasta 500 contactos)
2. Ve a: Audience → Signup forms → Embedded forms
3. Copia la URL del `action` del formulario
4. En `index.html`, busca `TU-MAILCHIMP-URL` y sustitúyelo

---

## PASO 4 — Subir a IONOS (elguardiandechamberi.com)

### Crear usuario FTP en IONOS (importante: NO uses tu contraseña principal)
1. Ve a my.ionos.es → Hosting → FTP → Crear usuario FTP
2. Nombre: `guardian-web`
3. Directorio: `/` (raíz del dominio)
4. Anota usuario y contraseña que crees

### Subir los archivos
Abre CMD o PowerShell en la carpeta `guardian-chamberi/` y ejecuta:

```cmd
set FTP_HOST=ftp.ionos.es
set FTP_USER=tu_usuario_ftp
set FTP_PASS=tu_contraseña_ftp
python subir_ionos.py
```

O edita directamente `subir_ionos.py` y rellena FTP_USER y FTP_PASS.

---

## Vista previa local (sin subir nada)

Simplemente abre `index.html` con tu navegador (doble clic).
Funcionará perfectamente para ver la web antes de publicarla.
