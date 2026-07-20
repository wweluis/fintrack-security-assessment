# 06 — # Plan de Respuesta a Incidentes

## Decisión que permite tomar este documento

Este documento define quién hace qué durante los primeros 60 minutos después de detectar un incidente de seguridad en FinTrack.

El objetivo es reducir el impacto del incidente, proteger la información financiera de los clientes, mantener la disponibilidad del servicio y asegurar una respuesta coordinada.

---

# Roles

FinTrack cuenta con un equipo pequeño de TI conformado por 4 personas. Cada integrante tiene responsabilidades específicas durante un incidente.

| Rol | Responsabilidad | Quién |
|---|---|---|
| Líder de respuesta a incidentes | Coordina las acciones, toma decisiones críticas, define prioridades y comunica el estado del incidente. | Responsable de TI |
| Analista de seguridad | Investiga el origen del incidente, revisa logs, identifica indicadores de compromiso y determina el alcance. | Especialista de Seguridad |
| Administrador de infraestructura | Ejecuta acciones técnicas: aislamiento de equipos, bloqueo de accesos, respaldos y recuperación de servicios. | Administrador de Sistemas |
| Responsable de comunicación y negocio | Coordina comunicación interna, informa a dirección y gestiona comunicación con clientes o proveedores si aplica. | Coordinador Operativo |

---

# Fases de respuesta al incidente

## 1. Detección

**Objetivo:** Confirmar que existe un incidente y determinar su gravedad.

Acciones en FinTrack:

- Revisar alertas de seguridad, registros de acceso y actividad sospechosa.
- Confirmar si existe compromiso de cuentas, sistemas o información financiera.
- Identificar:
  - Usuario afectado.
  - Sistema comprometido.
  - Fecha y hora del evento.
  - Tipo de ataque.

Ejemplo aplicado a FinTrack:

Se detecta un correo de phishing enviado a un empleado del área financiera. El atacante obtiene credenciales de acceso e intenta ingresar al sistema administrativo.

Durante los primeros 15 minutos:

- El analista de seguridad revisa logs de autenticación.
- Se identifica la cuenta comprometida.
- Se clasifica como incidente de seguridad de alta prioridad.

---

# 2. Contención

**Objetivo:** Evitar que el atacante continúe causando daños.

Acciones en FinTrack:

- Bloquear temporalmente la cuenta comprometida.
- Revocar sesiones activas.
- Cambiar credenciales afectadas.
- Aislar equipos sospechosos de la red.
- Bloquear direcciones IP maliciosas.

Durante los primeros 30 minutos:

- Infraestructura desconecta equipos comprometidos.
- Seguridad recopila evidencia antes de realizar cambios.
- El líder del incidente aprueba medidas de emergencia.

---

# 3. Erradicación

**Objetivo:** Eliminar completamente la causa del incidente.

Acciones en FinTrack:

- Eliminar malware encontrado.
- Corregir vulnerabilidades utilizadas por el atacante.
- Actualizar contraseñas y permisos.
- Revisar configuraciones de seguridad.
- Aplicar parches pendientes.

Ejemplo:

Si el atacante ingresó mediante una contraseña robada:

- Se fuerza cambio de contraseña.
- Se habilita autenticación multifactor.
- Se revisan accesos realizados con esa cuenta.

---

# 4. Recuperación

**Objetivo:** Restaurar los servicios normales de FinTrack de forma segura.

Acciones:

- Restaurar sistemas desde respaldos verificados.
- Confirmar que no existen accesos no autorizados.
- Monitorear actividad durante las siguientes horas.
- Validar funcionamiento de aplicaciones financieras.

Antes de regresar a operación:

- Seguridad confirma que el atacante fue eliminado.
- Infraestructura valida servidores y bases de datos.
- Negocio confirma disponibilidad del servicio.

---

# 5. Lecciones aprendidas

**Objetivo:** Evitar que el incidente vuelva a ocurrir.

Después del incidente se realiza una reunión para analizar:

- Qué ocurrió.
- Cómo ingresó el atacante.
- Qué controles fallaron.
- Qué mejoras deben implementarse.

Acciones posibles:

- Capacitación contra phishing.
- Mejoras en monitoreo de logs.
- Implementación de MFA obligatorio.
- Actualización de políticas de seguridad.
- Mejora de respaldos.

Se documenta:

- Línea de tiempo del incidente.
- Evidencias encontradas.
- Decisiones tomadas.
- Acciones preventivas futuras.

---

# Cómo escalar

Un incidente debe escalarse cuando:

| Situación | Escalar a | Motivo | Canal |
|---|---|---|---|
| Compromiso de cuentas internas | Responsable de TI | Tomar decisiones y controlar accesos | Teléfono interno / Chat corporativo |
| Fuga de información financiera | Dirección de FinTrack | Evaluar impacto legal y clientes afectados | Reunión urgente |
| Ataque activo contra servidores | Administrador de Infraestructura | Aplicar medidas técnicas inmediatas | Canal de emergencia TI |
| Posible incumplimiento legal | Responsable legal externo | Evaluar obligaciones regulatorias | Correo corporativo |
| Ataque de proveedor externo | Contacto del proveedor | Coordinar investigación conjunta | Mesa de soporte del proveedor |

---

# Contactos

## Contactos internos

| Contacto | Responsabilidad | Canal |
|---|---|---|
| Responsable de TI | Coordinación general del incidente | Teléfono interno / Chat corporativo |
| Analista de Seguridad | Investigación y análisis técnico | Chat seguridad |
| Administrador de Sistemas | Infraestructura y recuperación | Canal TI |
| Dirección FinTrack | Decisiones de negocio | Reunión urgente |

---

## Contactos externos

| Contacto | Cuándo contactar |
|---|---|
| Proveedor de infraestructura cloud | Cuando exista afectación de servidores o servicios alojados |
| Proveedor de seguridad | Cuando se requiera análisis especializado |
| Autoridades correspondientes | Cuando exista robo de información o impacto legal |
| Clientes afectados | Cuando exista evidencia de exposición de datos |

---

# Línea de tiempo primeros 60 minutos

| Tiempo | Acción |
|---|---|
| 0 - 15 minutos | Detectar, validar y clasificar incidente |
| 15 - 30 minutos | Contener amenaza y bloquear accesos |
| 30 - 45 minutos | Investigar alcance y eliminar causa inicial |
| 45 - 60 minutos | Recuperar servicios críticos y comunicar estado |

## Cómo escalar
[Cuándo se escala, a quién, por qué canal.]

## Contactos
[A quién se avisa: interno y externo.]
