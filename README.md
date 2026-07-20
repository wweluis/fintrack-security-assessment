# Evaluación de Seguridad — FinTrack Solutions

> Repositorio de portafolio. Evaluación de seguridad para FinTrack Solutions,
> una fintech ficticia. Documenta un proyecto de consultoría de principio a fin.

## Sobre este proyecto
FinTrack Solutions es una fintech ficticia dedicada a gestionar información y operaciones financieras digitales para sus clientes. Esta evaluación analiza los riesgos de seguridad a los que está expuesta la organización, considerando sus activos críticos, arquitectura, amenazas actuales y controles necesarios.

El objetivo de este proyecto es identificar vulnerabilidades, priorizar riesgos y proponer una estrategia de seguridad práctica basada en la realidad de una empresa pequeña, incluyendo políticas, respuesta ante incidentes y recomendaciones para mejorar su postura de seguridad.

Este repositorio contiene el análisis completo realizado durante el proceso de evaluación de seguridad.

## Estructura
- `01-business-case.md` — el cliente, sus activos y el alcance
- `02-architecture/` — arquitectura y superficie de ataque
- `03-risk-analysis/` — modelo de amenazas y registro de riesgos R1–R6
- `04-security-controls/` — controles propuestos C1–C6
- `05-policies/` — políticas mínimas viables
- `06-incident-response/` — plan de respuesta y playbook
- `07-postmortem/` — postmortem del incidente
- `08-recommendations.md` — recomendaciones finales

## Tesis
El principal hallazgo de esta evaluación es que **el perímetro de seguridad de FinTrack no está definido por la red, sino por la identidad de sus usuarios y el control de sus accesos**.

Los ataques de phishing, robo de credenciales y accesos no autorizados representan una amenaza mayor que los ataques tradicionales al perímetro, por lo que FinTrack debe priorizar controles como MFA, monitoreo de identidad, gestión de accesos y capacitación continua.


## Autor
**Luis Alvarado**

- LinkedIn: www.linkedin.com/in/luis-alvarado-14a44a317
- GitHub: https://github.com/wweluis


