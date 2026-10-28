# StudyFlow — Grupos de estudio entre familias

Esta versión añade el inicio del flujo de grupos independientes: crear grupo con código, solicitar unirse con código y una bandeja de autorización del padre/madre. Cada familia conserva sus colecciones privadas.

## Archivos modificados
- `app/index.html`: tarjeta de grupos y formularios de creación/solicitud; panel de autorizaciones para padre/madre.
- `app/firebase.js`: acceso raíz de Firestore para las colecciones de grupos, códigos y solicitudes.
- `firebase/firestore.rules`: reglas para códigos, grupos, solicitudes, miembros y autorizaciones familiares.

## Antes de desplegar
1. Haz copia de seguridad del repositorio y de `firebase/firestore.rules`.
2. Conserva tu `app/firebase-config.js` actual.
3. Revisa las reglas en el emulador de Firebase con dos familias de prueba antes de desplegarlas en producción.
4. Ejecuta desde la carpeta `firebase`: `firebase deploy --only firestore:rules`.
5. Publica `app/index.html` y `app/firebase.js` en GitHub Pages.

## Estado de implementación
Esta entrega incorpora creación de grupo, código y solicitud con autorización familiar. La aceptación final por el creador, la publicación de métricas académicas al grupo y el ranking compartido aún requieren completar y probar su flujo de punta a punta. No se deben compartir notas ni tareas de otra familia hasta que esa parte esté implementada.
