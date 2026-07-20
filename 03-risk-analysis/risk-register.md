# 03 — Registro de Riesgos

**Decisión que permite tomar este documento:** en qué orden gastar el esfuerzo limitado del equipo.

> Regla: un control sin riesgo asociado no entra al informe. Una política
> sin un riesgo que la exija, tampoco. Seis riesgos bien argumentados valen
> más que veinte listados.

---

## Resumen

| ID | Riesgo                               | Prob. | Impacto | Nivel   | Control |
| -- | ------------------------------------ | ----- | ------- | ------- | ------- |
| R1 | Phishing y robo de credenciales      | Alta  | Alto    | Crítico | C1      |
| R2 | Acceso no autorizado a la aplicación | Media | Alto    | Alto    | C2      |
| R3 | Malware o ransomware                 | Media | Alto    | Alto    | C3      |
| R4 | Falta de monitoreo y detección       | Alta  | Alto    | Crítico | C4      |
| R5 | Exposición de datos por terceros     | Media | Alto    | Alto    | C5      |
| R6 | Copias de seguridad insuficientes    | Media | Alto    | Alto    | C6      |


## R1 · Phishing y robo de credenciales
| Campo                       | Valor                                                                                                                                                 |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Descripción**             | Un atacante engaña a un empleado para obtener sus credenciales corporativas mediante un correo electrónico fraudulento.                               |
| **Activos**                 | A4, A1 y A2                                                                                                                                           |
| **Propiedad violada (CID)** | Confidencialidad                                                                                                                                      |
| **Probabilidad**            | **Alta** — El incidente descrito en el caso de FinTrack demuestra que este riesgo ya ocurrió.                                                         |
| **Impacto**                 | **Alto** — El atacante puede acceder a información financiera y utilizar el correo corporativo para nuevas campañas.                                  |
| **Nivel**                   | Crítico                                                                                                                                               |
| **Escenario concreto**      | Un empleado del área financiera introduce sus credenciales en un sitio falso y el atacante mantiene acceso al correo corporativo durante varios días. |
| **Control**                 | C1 – Implementación de autenticación multifactor (MFA) y capacitación periódica contra phishing.                                                      |


## R2 · Acceso no autorizado a la aplicación
| Campo                       | Valor                                                                                                        |
| --------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Descripción**             | Un atacante explota vulnerabilidades en la aplicación web o en la API para acceder a funciones restringidas. |
| **Activos**                 | A2 y A3                                                                                                      |
| **Propiedad violada (CID)** | Integridad                                                                                                   |
| **Probabilidad**            | Media — Las aplicaciones expuestas a Internet son objetivos frecuentes.                                      |
| **Impacto**                 | Alto — Podría alterar operaciones financieras o acceder a datos sensibles.                                   |
| **Nivel**                   | Alto                                                                                                         |
| **Escenario concreto**      | Un atacante aprovecha una falla de autenticación para acceder a funciones administrativas.                   |
| **Control**                 | C2 – Revisión de autenticación, autorización y protección de la API.                                         |

Nota de análisis: La seguridad debe implementarse tanto en la aplicación como en la API.

## R3 · Malware o ransomware
| Campo                       | Valor                                                                                               |
| --------------------------- | --------------------------------------------------------------------------------------------------- |
| **Descripción**             | Equipos de empleados son infectados con malware o ransomware que afecta la continuidad del negocio. |
| **Activos**                 | A3 y A1                                                                                             |
| **Propiedad violada (CID)** | Disponibilidad                                                                                      |
| **Probabilidad**            | Media — Es una amenaza frecuente para organizaciones de todos los tamaños.                          |
| **Impacto**                 | Alto — Puede interrumpir los servicios y provocar pérdida de información.                           |
| **Nivel**                   | Alto                                                                                                |
| **Escenario concreto**      | Un archivo malicioso cifra la información de un servidor crítico.                                   |
| **Control**                 | C3 – Protección de endpoints (EDR/antivirus) y copias de seguridad verificadas.                     |

Nota de análisis: La recuperación depende de contar con respaldos íntegros y probados.

## R4 · Falta de monitoreo y detección
| Campo                       | Valor                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------- |
| **Descripción**             | Actividades maliciosas pasan desapercibidas por no existir registros ni alertas.        |
| **Activos**                 | Todos los activos críticos                                                              |
| **Propiedad violada (CID)** | Disponibilidad                                                                          |
| **Probabilidad**            | Alta — El incidente de FinTrack no fue detectado por herramientas de monitoreo.         |
| **Impacto**                 | Alto — Aumenta el tiempo de permanencia del atacante y dificulta la investigación.      |
| **Nivel**                   | Crítico                                                                                 |
| **Escenario concreto**      | Un atacante permanece varios días con acceso al correo corporativo sin generar alertas. |
| **Control**                 | C4 – Centralización de registros y monitoreo continuo.                                  |

Nota de análisis: No detectar un incidente a tiempo amplifica el impacto de cualquier otro riesgo.

## R5 · Exposición de datos por terceros
| Campo                       | Valor                                                                                      |
| --------------------------- | ------------------------------------------------------------------------------------------ |
| **Descripción**             | Una integración con proveedores externos compromete información de clientes.               |
| **Activos**                 | A5 y A1                                                                                    |
| **Propiedad violada (CID)** | Confidencialidad                                                                           |
| **Probabilidad**            | Media — FinTrack depende de servicios externos para su operación.                          |
| **Impacto**                 | Alto — Una falla en un tercero puede afectar la reputación y la confianza de los clientes. |
| **Nivel**                   | Alto                                                                                       |
| **Escenario concreto**      | Un proveedor de correo sufre una vulnerabilidad que expone información compartida.         |
| **Control**                 | C5 – Evaluación de proveedores y revisión periódica de accesos e integraciones.            |

Nota de análisis: La seguridad también depende de la cadena de suministro digital.

## R6 · Copias de seguridad insuficientes
| Campo                       | Valor                                                                                                                   |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Descripción**             | La organización no puede recuperar información crítica después de un incidente.                                         |
| **Activos**                 | A1, A2 y A3                                                                                                             |
| **Propiedad violada (CID)** | Disponibilidad                                                                                                          |
| **Probabilidad**            | Media — Sin pruebas periódicas de restauración, los respaldos pueden ser ineficaces.                                    |
| **Impacto**                 | Alto — La pérdida de información financiera afectaría la continuidad del negocio.                                       |
| **Nivel**                   | Alto                                                                                                                    |
| **Escenario concreto**      | Tras un ataque de ransomware, la empresa intenta restaurar la información y descubre que las copias no son utilizables. |
| **Control**                 | C6 – Política de respaldos, pruebas de restauración y almacenamiento seguro.                                            |

Nota de análisis: Un respaldo que nunca se ha probado no garantiza la recuperación del negocio.

## Argumento de priorización

Los riesgos R1 y R4 se atienden primero porque ya se materializaron en el incidente descrito para FinTrack y representan la mayor exposición actual. En segundo lugar se priorizan R2 y R3 por su impacto sobre la aplicación y la continuidad del negocio. Finalmente se abordan R5 y R6 para fortalecer la resiliencia frente a incidentes que involucren terceros o requieran procesos de recuperación.


## Riesgos evaluados y descartados

| Riesgo considerado                 | Por qué no entra al registro                                                                                            |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Ataques de Estados                 | FinTrack no representa un objetivo estratégico y los controles necesarios exceden su capacidad operativa y presupuesto. |
| Ataques físicos al centro de datos | La infraestructura se encuentra en un proveedor de nube pública que ya implementa controles físicos especializados.     |



# Registro de riesgos

| ID | Riesgo | Probabilidad | Impacto |
|----|---------|--------------|---------|
| R1 | Phishing contra empleado financiero | Alta | Alto |
| R2 | Robo de credenciales | Alta | Alto |
| R3 | Malware en equipo corporativo | Media | Alto |
| R4 | Acceso no autorizado a sistemas internos | Media | Alto |
| R5 | Ransomware en servidores | Media | Crítico |

## Riesgo principal del caso

El incidente simulado de FinTrack se centra en **R1 (phishing)**, donde un empleado del área financiera entrega sus credenciales a un atacante.
