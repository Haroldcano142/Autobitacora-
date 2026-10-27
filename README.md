# AutoBitácora — prototipo PWA

## Qué incluye
- Ficha de cliente y vehículo.
- Checklist de recepción.
- Conceptos y total de costos en MXN.
- Campos para reporte de escáner y contenido de QR.
- Notas de entrega, nombres de firma y vista de impresión para PDF.
- Búsqueda, guardado local y exportación/importación de respaldo JSON.
- Manifiesto y service worker básicos para instalación PWA.

## Límites importantes de esta versión
Esta es una primera maqueta funcional, no un sistema listo para producción:
- Los registros se guardan solo en el almacenamiento del navegador de este dispositivo.
- No hay cuenta, sincronización en nube ni autenticación real.
- Las notas privadas no están protegidas criptográficamente; no introducir información sensible.
- Las fotos y adjuntos no se guardan permanentemente todavía.
- El campo QR recibe contenido pegado manualmente; no escanea automáticamente con cámara.
- Las firmas son nombres escritos, no firmas manuscritas verificadas.
- El PDF se genera mediante imprimir/guardar como PDF del navegador.
- El service worker requiere HTTPS o localhost para funcionar correctamente.

## Cómo probar
Abre `index.html` en un navegador para probar la interfaz. Para probar instalación PWA, aloja estos archivos en un sitio HTTPS. En Android, abre la URL en Chrome y usa el menú ⋮ > **Instalar aplicación** o **Agregar a pantalla de inicio**.

## Siguiente etapa antes de uso real en taller
1. Publicar en hosting HTTPS.
2. Implementar autenticación y roles.
3. Base de datos y almacenamiento de archivos en nube.
4. Proteger notas privadas con permisos del servidor.
5. Añadir captura de cámara, QR y firmas manuscritas.
6. Probar restauración, permisos, privacidad y exportación PDF.

No usar datos reales de clientes hasta completar la seguridad y las copias de respaldo.
