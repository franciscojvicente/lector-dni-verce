# Lector de DNI — demo web

Sitio estático de un solo archivo (`index.html`). No requiere backend ni comando de build. La lectura ocurre en el navegador; ZXing se carga desde jsDelivr, por lo que hace falta conexión a internet al abrir la página.

## Publicar en GitHub y Vercel

1. En GitHub, crea un repositorio nuevo llamado `lector-dni-vercel`. Puede ser privado. Déjalo vacío, sin README, licencia ni `.gitignore` generados.
2. Abre una terminal en esta carpeta y ejecuta estos comandos. Reemplaza `TU-USUARIO` por tu usuario de GitHub:

```bash
git init -b main
git add index.html README.md
git commit -m "Publicar lector DNI"
git remote add origin https://github.com/TU-USUARIO/lector-dni-vercel.git
git push -u origin main
```

3. En Vercel, selecciona **Add New → Project**, importa el repositorio `lector-dni-vercel` y configura:
   - **Framework Preset:** Other
   - **Build Command:** vacío
   - **Output Directory:** `.` (si Vercel lo solicita)
4. Pulsa **Deploy**. Abre la URL `https://...vercel.app` desde el celular y acepta el permiso de cámara.

Si no quieres usar Git en tu PC, puedes crear el repositorio vacío en GitHub y subir `index.html` y `README.md` con **Add file → Upload files**; luego impórtalo en Vercel.

## Uso en el celular

Abre el enlace en Chrome (Android) o Safari (iPhone). Si WhatsApp lo abre en su navegador interno y no aparece la cámara, usa **Abrir en navegador**. La página solicita acceso a la cámara; la foto y el resultado se procesan localmente y no se envían a un servidor.

El lector reconoce QR, Data Matrix y PDF417. No autentica documentos y todavía no reconoce el código de barras lineal de la constancia electoral.
