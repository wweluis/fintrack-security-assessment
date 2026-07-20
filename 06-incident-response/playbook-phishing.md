# Playbook — Incidente de Phishing

## Objetivo

Establecer el procedimiento de respuesta cuando un empleado de FinTrack recibe, abre o interactúa con un correo electrónico de phishing que pueda comprometer credenciales, información financiera o acceso a sistemas internos.

Este playbook busca reducir el impacto del ataque durante los primeros minutos y asegurar una investigación adecuada.

---

# Cuándo se activa

Este procedimiento se activa cuando ocurre cualquiera de estas situaciones:

- Un empleado reporta haber recibido un correo sospechoso.
- Un usuario hace clic en un enlace malicioso recibido por correo.
- Un empleado introduce sus credenciales en una página falsa.
- Se detectan accesos anómalos asociados a una cuenta después de un correo sospechoso.
- El equipo de seguridad identifica una campaña de phishing dirigida a empleados de FinTrack.

Ejemplo:

Un empleado del área financiera recibe un correo aparentemente enviado por un proveedor, ingresa sus credenciales en un sitio falso y posteriormente aparecen intentos de acceso desde una ubicación desconocida.

---

# Pasos

## 1. Reporte inicial (primeros minutos)

**Persona que detecta el incidente:**

Debe:

- Informar inmediatamente al equipo de TI o seguridad.
- No eliminar el correo recibido.
- Guardar evidencia:
  - Remitente.
  - Asunto del correo.
  - Hora de recepción.
  - Enlace sospechoso.
  - Archivos adjuntos.

Canales de reporte:

- Chat interno de seguridad.
- Canal de incidentes TI.
- Comunicación directa con el responsable de TI.

---

## 2. Validación del incidente

El analista de seguridad debe:

- Revisar los encabezados del correo.
- Analizar enlaces y archivos adjuntos.
- Confirmar si corresponde a un intento de phishing.
- Identificar usuarios afectados.
- Revisar registros de acceso.

Datos importantes:

- Cuenta comprometida.
- Hora del posible acceso.
- Dirección IP utilizada.
- Sistemas afectados.

---

## 3. Contención

Si existe compromiso de credenciales:

- Bloquear temporalmente la cuenta afectada.
- Forzar cambio de contraseña.
- Cerrar sesiones activas.
- Revisar accesos recientes.
- Activar autenticación multifactor si está disponible.

Si existen múltiples usuarios afectados:

- Alertar al personal.
- Bloquear dominios o direcciones utilizadas por el atacante.
- Buscar mensajes similares en los buzones corporativos.

---

## 4. Erradicación

Acciones:

- Eliminar correos maliciosos de los buzones corporativos.
- Bloquear dominios utilizados en la campaña.
- Eliminar malware si existió ejecución de archivos.
- Corregir configuraciones inseguras.
- Actualizar controles de seguridad.

---

## 5. Recuperación

Antes de volver a operación normal:

- Confirmar que las cuentas no tienen accesos sospechosos.
- Verificar que no existan reglas maliciosas en el correo.
- Revisar movimientos o accesos financieros anormales.
- Mantener monitoreo reforzado durante las siguientes horas.

---

# Qué NO hacer

Errores comunes que pueden aumentar el impacto:

- ❌ Eliminar el correo antes de recopilar evidencia.
- ❌ Responder al atacante.
- ❌ Abrir nuevamente enlaces o archivos sospechosos para "comprobar".
- ❌ Continuar usando una cuenta posiblemente comprometida.
- ❌ Cambiar contraseñas sin revisar si el atacante mantiene una sesión activa.
- ❌ Ocultar el incidente por miedo a consecuencias.
- ❌ Compartir el correo malicioso con otros empleados sin advertencia.

---

# Después del incidente

Para el postmortem se debe documentar:

## Información del incidente

- Fecha y hora de detección.
- Persona que reportó.
- Usuarios afectados.
- Sistemas involucrados.

## Evidencias recopiladas

- Correo original.
- Remitente y dominio utilizado.
- URLs maliciosas.
- Archivos adjuntos.
- Logs de acceso.
- Direcciones IP sospechosas.

## Análisis

- Método utilizado por el atacante.
- Cómo obtuvo acceso.
- Qué información pudo estar comprometida.
- Tiempo de detección y respuesta.

## Mejoras propuestas

- Capacitación de empleados.
- Mejoras en filtros antiphishing.
- Implementación de MFA.
- Nuevas reglas de monitoreo.
- Actualización de políticas internas.

---

# Indicadores de éxito

El incidente se considera controlado cuando:

- La cuenta comprometida está asegurada.
- El acceso del atacante fue eliminado.
- No existen nuevas actividades sospechosas.
- La evidencia fue almacenada.
- Se generó un informe final del incidente.
