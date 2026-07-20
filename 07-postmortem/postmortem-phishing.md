# 07 — # Postmortem — Incidente de Phishing

## Cultura

Este postmortem utiliza un enfoque **blameless** (sin culpables).

El objetivo no es encontrar quién cometió un error, sino entender qué condiciones permitieron que el incidente ocurriera y qué mejoras deben implementarse para reducir la probabilidad de repetición.

---

# Resumen

FinTrack detectó un incidente de phishing dirigido a un empleado del área financiera mediante un correo que simulaba ser enviado por un proveedor conocido.

El atacante utilizó ingeniería social para obtener credenciales de acceso mediante una página falsa similar al portal corporativo.

La cuenta comprometida fue utilizada para realizar intentos de acceso no autorizados a sistemas internos.

El incidente fue contenido mediante bloqueo de la cuenta, revisión de registros y aplicación de medidas de seguridad adicionales.

---

# Línea de tiempo

| Hora | Evento |
|---|---|
| 08:15 | Empleado recibe correo sospechoso aparentemente enviado por un proveedor. |
| 08:20 | Usuario accede al enlace incluido en el correo e introduce credenciales. |
| 08:35 | El atacante intenta acceder al sistema utilizando las credenciales obtenidas. |
| 08:40 | El sistema detecta un acceso desde una ubicación inusual. |
| 08:45 | Equipo de TI inicia investigación del evento. |
| 09:00 | Se bloquea la cuenta comprometida y se cierran sesiones activas. |
| 09:30 | Se revisan logs para identificar accesos adicionales. |
| 10:30 | Se confirma la contención del incidente. |

---

# Impacto

## Sistemas afectados

- Cuenta corporativa de un empleado del área financiera.
- Sistema de autenticación interno.
- Correo corporativo.

## Pilares CID afectados

| Pilar | Impacto |
|---|---|
| Confidencialidad | Riesgo de exposición de credenciales e información financiera. |
| Integridad | Posibilidad de modificación o uso indebido de información. |
| Disponibilidad | No hubo interrupción significativa del servicio. |

Impacto general:

El incidente no provocó caída de servicios, pero representó un riesgo para la confidencialidad de la información y la seguridad de las cuentas internas.

---

# Causa raíz

La causa raíz no fue simplemente que un empleado abrió un enlace.

El incidente fue posible porque varios controles permitieron que una acción de ingeniería social tuviera impacto:

- Falta de autenticación multifactor obligatoria para todas las cuentas.
- Capacitación insuficiente sobre campañas de phishing avanzadas.
- Falta de alertas automáticas ante accesos desde ubicaciones anormales.
- Proceso de reporte de correos sospechosos no suficientemente visible.
- Dependencia excesiva de la detección humana.

El problema principal fue que el sistema no tenía suficientes capas de protección para detener el ataque después del primer error.

---

# Qué funcionó / qué no

| Funcionó | No funcionó |
|---|---|
| El equipo detectó accesos sospechosos mediante revisión de logs. | La cuenta comprometida no tenía MFA habilitado. |
| Existía un procedimiento inicial de respuesta. | Los filtros de correo no detectaron el mensaje malicioso. |
| El equipo pudo bloquear la cuenta rápidamente. | No existía suficiente entrenamiento contra phishing dirigido. |
| Los registros permitieron investigar el evento. | No había alertas automáticas de comportamiento anómalo. |

---

# Acciones correctivas

| Acción | Dueño | Riesgo que cierra |
|---|---|---|
| Implementar MFA obligatorio para cuentas internas. | Administrador de Sistemas | Robo de credenciales. |
| Realizar capacitaciones periódicas contra phishing. | Responsable de Seguridad | Ingeniería social. |
| Mejorar filtros antiphishing del correo corporativo. | Administrador de Infraestructura | Correos maliciosos. |
| Crear alertas por accesos sospechosos. | Analista de Seguridad | Uso indebido de cuentas. |
| Establecer un botón/proceso de reporte de phishing. | Responsable de TI | Retraso en detección. |
| Revisar permisos de usuarios y aplicar mínimo privilegio. | Responsable de Seguridad | Movimiento lateral del atacante. |
