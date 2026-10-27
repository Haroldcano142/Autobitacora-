# AutoBitácora — prototipo con integración inicial de Google Drive

## Antes de usar
Esta versión es un prototipo. No la uses todavía con datos reales de clientes. La página de GitHub Pages es pública y esta versión no implementa control de acceso por propietario ni un backend. Los expedientes guardados en Drive incluyen observaciones privadas; aunque los archivos creados por Drive API suelen ser privados por defecto, cualquier persona que tenga acceso a la cuenta o comparta esos archivos podría verlos. No compartas archivos de expedientes.

## Configurar en teléfono
1. En Google Cloud, habilita Google Drive API.
2. En Google Auth Platform, crea un cliente OAuth tipo Aplicación web.
3. En orígenes autorizados de JavaScript, agrega el origen real de tu sitio, por ejemplo `https://haroldcano142.github.io`. No añadas ruta `/autobitacora/` si tu web se publica en el dominio raíz.
4. En GitHub, abre `config.js` y toca editar (lápiz).
5. Sustituye `PEGA_AQUI_EL_ID_DE_CLIENTE.apps.googleusercontent.com` por el Client ID completo del cliente web. Es el ID público, no el secreto. Guarda con Commit changes.
6. Sube todos los archivos de esta carpeta a la raíz del repositorio, reemplazando los archivos existentes. Incluye `config.js`.
7. Abre la página y recarga. Pulsa “Conectar Google Drive” y autoriza el acceso `drive.file`.
8. Guarda un expediente de prueba sin datos reales; luego pulsa “Buscar expedientes en Drive” y comprueba que puedes cargarlo.

## Qué hace esta versión
- Conecta con Google Identity Services en el navegador.
- Solicita el permiso limitado `drive.file`.
- Guarda expedientes JSON en Drive y permite listarlos/cargarlos.
- No guarda el token de acceso en localStorage; tras recargar, hay que volver a conectar.
- El PDF de impresión excluye el contenido del campo de observaciones privadas.

## Limitaciones importantes
- Esta es una integración inicial, no una aplicación lista para producción.
- No implementa autenticación exclusiva de un propietario en la propia aplicación ni backend de seguridad.
- Los datos en localStorage y los respaldos JSON locales no están cifrados por esta app.
- Fotos y archivos adjuntos todavía no se suben a Drive.
- No compartas el ID secreto OAuth ni ningún token. Para una app web, el Client ID es público; el secreto no debe estar en código del navegador.
