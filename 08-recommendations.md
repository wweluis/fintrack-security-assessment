# 08 — Recomendaciones Finales

## Decisión que permite tomar este documento

Este documento permite al CTO de FinTrack decidir qué acciones de seguridad implementar, en qué orden y utilizando los recursos disponibles actualmente.

Las recomendaciones están priorizadas según impacto en la reducción de riesgos, esfuerzo requerido y tamaño de la organización.

---

# Resumen ejecutivo

FinTrack presenta una mayor exposición en riesgos relacionados con el factor humano, especialmente ataques de phishing dirigidos al personal financiero, robo de credenciales y falta de controles avanzados de monitoreo. El principal riesgo identificado es que una cuenta comprometida pueda permitir acceso no autorizado a información financiera y sistemas internos.

La primera prioridad debe ser fortalecer los controles básicos de seguridad: implementar autenticación multifactor (MFA), mejorar la capacitación contra phishing y centralizar los registros de seguridad para detectar comportamientos anómalos. Estas medidas reducen significativamente el riesgo sin requerir grandes inversiones.

FinTrack no debe iniciar con soluciones costosas o complejas como un SOC 24/7 tercerizado, ya que por el tamaño actual del negocio el costo supera el beneficio esperado. Primero debe consolidar controles fundamentales y procesos internos de respuesta antes de aumentar la complejidad tecnológica.

---

# Hoja de ruta

| Cuándo | Acción | Riesgo que cierra | Esfuerzo |
|---|---|---|---|
| Esta semana | Implementar MFA en cuentas administrativas y financieras. | Robo de credenciales por phishing. | Bajo |
| Esta semana | Crear proceso formal para reportar correos sospechosos. | Retraso en detección de phishing. | Bajo |
| Este mes | Realizar capacitación anti-phishing para empleados. | Ingeniería social y errores humanos. | Medio |
| Este mes | Centralizar logs de autenticación y sistemas críticos. | Falta de visibilidad ante accesos sospechosos. | Medio |
| Este trimestre | Implementar EDR en equipos críticos. | Malware y compromiso de dispositivos. | Medio |
| Este trimestre | Mejorar segmentación de red interna. | Movimiento lateral del atacante. | Alto |
| 12 meses | Evaluar soluciones avanzadas de monitoreo y automatización. | Ataques sofisticados futuros. | Alto |

---

# Lo que deliberadamente no recomendamos

No todas las soluciones de seguridad son adecuadas para FinTrack en este momento. Las siguientes opciones fueron descartadas considerando tamaño, costo y madurez actual.

| Descartado | Por qué |
|---|---|
| SOC 24/7 tercerizado | El costo operativo es elevado para el tamaño actual de FinTrack y existen controles prioritarios que deben implementarse primero. |
| Comprar múltiples herramientas de seguridad sin integración | Aumentaría la complejidad sin resolver los riesgos principales identificados. |
| Implementar controles excesivamente restrictivos | Podría afectar la productividad sin reducir proporcionalmente el riesgo. |
| Auditorías constantes externas sin preparación interna | No generan suficiente valor mientras no existan procesos básicos consolidados. |

---

# Recomendaciones priorizadas

## Alta prioridad

### Implementar MFA

**Motivo:**

Reduce el impacto de ataques de phishing porque una contraseña robada no sería suficiente para acceder a los sistemas.

**Riesgo que cierra:**

- Robo de credenciales.
- Acceso no autorizado.

---

### Capacitación anti-phishing

**Motivo:**

El personal es una línea de defensa importante. Los ataques actuales utilizan técnicas de ingeniería social dirigidas.

**Riesgo que cierra:**

- Phishing.
- Ingeniería social.
- Compromiso de cuentas.

---

### Centralizar logs

**Motivo:**

Permite detectar accesos anormales, investigar incidentes y responder más rápido.

**Riesgo que cierra:**

- Falta de monitoreo.
- Detección tardía.

---

# Media prioridad

## Implementar EDR en equipos

**Motivo:**

Proporciona detección y respuesta frente a malware y actividades sospechosas en dispositivos.

**Riesgo que cierra:**

- Malware.
- Compromiso de endpoints.

---

## Segmentación de red

**Motivo:**

Limita el movimiento de un atacante dentro de la infraestructura si logra acceder a un equipo.

**Riesgo que cierra:**

- Movimiento lateral.
- Propagación de ataques.

---

# No recomendado actualmente

## SOC 24/7 tercerizado

No se recomienda actualmente para FinTrack debido al tamaño del negocio y al costo elevado frente al beneficio esperado.

Antes de considerar esta inversión, FinTrack debe fortalecer controles básicos:

- MFA.
- Gestión de accesos.
- Monitoreo de logs.
- Capacitación.
- Procesos de respuesta a incidentes.
