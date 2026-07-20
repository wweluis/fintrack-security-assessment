# 04 — Controles de Seguridad Propuestos

**Decisión que permite tomar este documento:** seleccionar los controles de seguridad que reducen los riesgos identificados, priorizando aquellos que FinTrack puede implementar y mantener con su equipo y presupuesto actuales.

> Regla: cada control cita el riesgo R# que mitiga. Por cada control, las
> opciones consideradas CON su pro y su contra. Si una opción no tiene contra,
> no la pensaste bien.

---

## C1 · Autenticación Multifactor (MFA) y capacitación — mitiga R1

**Objetivo:** Reducir el riesgo de robo de credenciales mediante phishing.

| Opción                | Pro                                                                             | Contra                                                      |
| --------------------- | ------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| A. Solo capacitación  | Bajo costo                                                                      | No evita el uso de credenciales robadas                     |
| B. MFA + capacitación | Bloquea la mayoría de accesos no autorizados incluso si la contraseña es robada | Requiere configuración inicial y adaptación de los usuarios |


> **Recomendación:** Implementar MFA para todos los empleados junto con campañas periódicas de concienciación sobre phishing. Es la mejor relación entre costo y beneficio para una empresa del tamaño de FinTrack.
> **Cuándo:** Esta semana.

---

## C2 · Fortalecer autenticación y autorización de la aplicación — mitiga R2
Objetivo: Evitar accesos no autorizados a la aplicación y la API.

| Opción                                         | Pro                                           | Contra                                      |
| ---------------------------------------------- | --------------------------------------------- | ------------------------------------------- |
| A. Revisiones manuales                         | Sin costo adicional                           | Dependen del conocimiento del desarrollador |
| B. Revisiones de código + pruebas de seguridad | Detectan vulnerabilidades antes de producción | Requieren tiempo adicional en el desarrollo |

Recomendación: Incorporar revisiones de seguridad en el ciclo de desarrollo y validar la autenticación y autorización antes de cada despliegue.

Cuándo: Este mes.

## C3 · Protección de endpoints y copias de seguridad — mitiga R3

Objetivo: Reducir el impacto de malware y ransomware.
| Opción                                   | Pro                                         | Contra                                          |
| ---------------------------------------- | ------------------------------------------- | ----------------------------------------------- |
| A. Antivirus tradicional                 | Fácil de implementar                        | Protección limitada frente a amenazas avanzadas |
| B. EDR + copias de seguridad verificadas | Mayor capacidad de detección y recuperación | Mayor costo y administración                    |

Recomendación: Mantener protección antimalware actual y complementar con copias de seguridad verificadas periódicamente. Si el presupuesto lo permite, evolucionar hacia una solución EDR.

Cuándo: Este trimestre.

## C4 · Monitoreo y centralización de registros — mitiga R4

Objetivo: Detectar actividades sospechosas de forma temprana.

| Opción                           | Pro                                                     | Contra                           |
| -------------------------------- | ------------------------------------------------------- | -------------------------------- |
| A. Revisar registros manualmente | Sin costo adicional                                     | Poco eficiente y fácil de omitir |
| B. Centralizar logs con alertas  | Detección más rápida y mejor capacidad de investigación | Requiere configuración inicial   |

Recomendación: Centralizar los registros y configurar alertas para eventos críticos, priorizando herramientas compatibles con el tamaño del equipo.

Cuándo: Este mes.

## C5 · Gestión de proveedores y accesos de terceros — mitiga R5
Objetivo: Reducir el riesgo derivado de servicios externos.

| Opción                                 | Pro                                             | Contra                                     |
| -------------------------------------- | ----------------------------------------------- | ------------------------------------------ |
| A. Confiar en los proveedores          | Sin esfuerzo adicional                          | No permite identificar riesgos de terceros |
| B. Evaluación periódica de proveedores | Mejora el control sobre la cadena de suministro | Requiere revisiones programadas            |

Recomendación: Revisar periódicamente los accesos e integraciones con terceros y documentar los riesgos asociados.

Cuándo: Este trimestre.

## C6 · Política de copias de seguridad y pruebas de restauración — mitiga R6
Objetivo: Garantizar la recuperación del negocio después de un incidente.

| Opción                                              | Pro                                     | Contra                          |
| --------------------------------------------------- | --------------------------------------- | ------------------------------- |
| A. Realizar respaldos sin verificarlos              | Fácil de implementar                    | No garantiza la recuperación    |
| B. Respaldos con pruebas periódicas de restauración | Aumenta la confianza en la recuperación | Consume tiempo del equipo de TI |

Recomendación: Implementar una política de respaldos con pruebas de restauración programadas y almacenamiento seguro.

Cuándo: Este trimestre.

## Resumen: qué se hace y cuándo

| Cuándo         | Acciones                                                                       | Riesgos que atacan |
| -------------- | ------------------------------------------------------------------------------ | ------------------ |
| Esta semana    | Implementar MFA y realizar capacitación básica contra phishing                 | R1                 |
| Este mes       | Revisar autenticación de la aplicación y centralizar registros                 | R2, R4             |
| Este trimestre | Mejorar respaldos, evaluar proveedores y fortalecer la protección de endpoints | R3, R5, R6         |


## Lo que deliberadamente NO recomendamos
| Descartado                                                                | Por qué                                                                                            |
| ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Certificación ISO 27001 inmediata                                         | FinTrack aún no cuenta con procesos maduros; primero debe implementar controles básicos.           |
| Centro de operaciones de seguridad (SOC) 24/7                             | El costo y la complejidad superan la capacidad de una empresa de 45 empleados.                     |
| Herramientas de seguridad de nivel empresarial con licencias muy costosas | Existen alternativas más económicas que cubren adecuadamente las necesidades actuales de FinTrack. |
| Red Team permanente                                                       | Antes es más importante fortalecer los controles básicos y la capacidad de detección.              |

