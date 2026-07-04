# Gestión automatizada de feedback de diseño

**Autor:** Manuel González Platero  
**Diplomatura en Diseño de Procesos de Negocios con Plataformas Visuales de Automatización e IA Agéntica**  
FCE-UBA · Cohorte 2026

---

## ¿Qué problema resuelve?

El equipo de diseño de producto trabaja con múltiples features en simultáneo. El feedback llega por tres canales — comentarios en Figma, transcripciones de Google Meet y @menciones en documentos de especificaciones técnicas en Google Drive — de forma fragmentada y sin un sistema que lo centralice. El resultado: feedback que se pierde por volumen, accionables que nunca se ejecutan, y decisiones sin trazabilidad.

Este proyecto automatiza la captura, clasificación y gestión de ese feedback usando n8n, Claude API y Trello.

---

## ¿Cómo funciona?

Todos los días a las 18hs, n8n se activa automáticamente y:

1. Captura los comentarios nuevos de Figma, las transcripciones de Google Meet y las @menciones de Google Drive del día
2. Envía cada item a Claude API, que lo clasifica por tipo y prioridad según una taxonomía predefinida
3. Crea una tarjeta en Trello con título, descripción, fuente de origen, prioridad y diseñador responsable

Los lunes, el equipo revisa el tablero, valida las prioridades sugeridas por la IA y decide qué se ejecuta.

---

## Taxonomía de clasificación

| Tipo de feedback | Prioridad |
|---|---|
| Rediseño | Alta |
| Cambio funcional | Media |
| Writing / copy | Baja |
| Tamaños / espaciados | Mínima |
| Sin contexto suficiente | Revisar |

---

## Herramientas utilizadas

- **n8n** — orquestación del flujo
- **Figma API** — captura de comentarios
- **Google Meet / Drive API** — captura de transcripciones y @menciones
- **Claude API** — clasificación y redacción de tarjetas
- **Trello** — gestión y trazabilidad del feedback

---

## Contexto

El proceso descripto refleja una situación real del equipo de diseño. Por políticas de seguridad de la empresa, el escenario de implementación usa cuentas personales con datos ficticios representativos.

---

## Documentación

El informe completo con diagnóstico, metodología y análisis crítico está disponible en `TP_Manuel_Gonzalez_Platero.pdf`.
