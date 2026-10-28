# StudyFlow: avatar y grupos de estudio

## Avatar del estudiante incluido
- En Ajustes del estudiante se puede elegir entre 16 avatares ilustrativos (emojis).
- La selección se guarda dentro de `settings.avatar` con el perfil y se muestra en la cabecera y el saludo.
- No requiere cambios en las reglas de Firestore.

## Requisito funcional acordado para grupos entre familias
La participación en un grupo debe requerir autorización del padre/madre. El flujo previsto es:
1. Un estudiante crea un grupo (nombre, grado y código aleatorio no secuencial).
2. Otro estudiante ingresa el código y solicita unirse; no obtiene acceso al progreso por ingresar el código.
3. Su padre/madre autoriza o rechaza desde su cuenta familiar.
4. El creador/moderador del grupo acepta la solicitud.
5. Solo después de ambas aprobaciones se comparte el resumen académico mínimo autorizado (avatar, nombre elegido, puntos, tareas completadas y promedio si se autoriza).
6. Cada familia conserva privados sus datos y puede revocar la participación.

**Nota:** el flujo entre familias no se activa con este ZIP. Requiere implementar colecciones globales de grupos y solicitudes, más reglas Firestore probadas para autorización parental y acceso mínimo. No se deben reutilizar las invitaciones actuales `studyPeers`, que están limitadas a una familia.
