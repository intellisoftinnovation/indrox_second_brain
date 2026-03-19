# Deal Rescue automático: n8n detecta deals calientes sin actividad y genera el mensaje de seguimiento por IA

**Categoría:** #operaciones
**Fecha:** 2026-03-17 05:14
**Impacto:** alto
**Estado:** pendiente

## Descripción

El problema más silencioso del pipeline de una empresa pequeña no es conseguir leads — es que los deals calientes se enfrían por falta de seguimiento sistemático. Con un flujo en n8n que monitorea el CRM cada día y avisa a Andre por Slack cuando un deal lleva +5 días sin actividad — con el contexto del deal y un mensaje de seguimiento generado por Claude listo para enviar —, ningún prospecto se pierde por olvido. Se estima que recuperar el 20% de los deals que se enfrían sin respuesta equivale a 1-2 proyectos extras al trimestre sin costo de adquisición.

## Cómo Ejecutar

1. Construir el flujo esta semana en n8n (2-3h de desarrollo): conectar al CRM actual de Indrox (Notion, HubSpot o Google Sheets) → filtrar deals con estado 'en conversación' o 'propuesta enviada' donde la última actividad registrada tenga más de 5 días → para cada uno, llamar a la API de Claude con prompt: 'Genera un mensaje de seguimiento de 3 líneas para [nombre], [empresa], sector [X], última interacción: [resumen]. Tono directo, no ansioso. Incluir referencia específica a la última conversación.' → Enviar resumen en Slack a Andre con el mensaje listo para copiar y enviar.
2. Definir los estados de deal que activan la alerta (solo los activos, no los perdidos ni los cerrados) y la frecuencia del check (diario a las 8am Lima). Configurar una segunda alerta a los 10 días si el deal sigue sin actividad — ese es el punto de decisión: marcar como perdido o escalar con un canal diferente (llamada, gifting físico, LinkedIn DM).
3. En la primera semana de operación: revisar cada mensaje generado por IA antes de enviar para calibrar el tono. Después de 10 seguimientos validados, activar en modo semi-automático: Andre solo aprueba o descarta con un emoji de reacción en Slack. Meta: cero deals calientes >7 días sin actividad registrada en el CRM.

## Ideas Relacionadas

- [[Sales playbook por vertical kit de ventas estandarizado para cerrar sin improvis]]
- [[Modelo de retainer mensual post-proyecto para generar MRR predecible]]
- [[Demo environment live por vertical cierra sin improvisar, delega sin riesgo]]
- [[Generador de propuestas con IA de 4 horas a 30 minutos por propuesta usando Neur]]
- [[Secuencia automática post-firma de la firma al upsell en 30 días sin esfuerzo ma]]