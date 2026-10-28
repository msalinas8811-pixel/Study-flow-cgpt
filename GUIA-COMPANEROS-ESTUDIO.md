# StudyFlow — Compañeros de estudio

## Funciones incluidas
- Desde el inicio del perfil estudiante aparece la tarjeta **Compañeros de estudio**.
- Se puede invitar a otro estudiante vinculado a la misma familia StudyFlow.
- El estudiante receptor puede aceptar o rechazar la invitación.
- Cuando ambos aceptan, aparece un ranking de compañeros conectados con promedio de notas, tareas completadas y puntos combinados.
- La regla `families/{fid}/studyPeers/{id}` limita la creación a estudiantes de la familia y permite al receptor cambiar el estado de una invitación pendiente.

## Publicación
1. Respalda el repositorio actual.
2. Copia `app/index.html` y `firebase/firestore.rules` del ZIP al repositorio.
3. Conserva `app/firebase-config.js` y el resto de tu configuración actual.
4. Publica reglas: `firebase deploy --only firestore:rules` desde la carpeta `firebase`.
5. Publica el sitio desde GitHub Pages.
6. Prueba con dos cuentas de estudiante ya vinculadas a la misma familia: una envía invitación, la otra acepta y ambas deben ver la tarjeta del ranking.

## Alcance y privacidad
Esta primera versión permite invitar estudiantes de la **misma familia StudyFlow**. No permite invitar estudiantes de otras familias ni crea una comunidad pública. El ranking es orientativo, calculado en el cliente a partir de los datos de progreso disponibles; debe probarse con datos reales antes de utilizarse para decisiones académicas. No se comparte información fuera de los miembros de la familia y compañeros aceptados según la interfaz, aunque las reglas de datos familiares existentes ya permiten a los miembros de la misma familia consultar los datos académicos familiares.
