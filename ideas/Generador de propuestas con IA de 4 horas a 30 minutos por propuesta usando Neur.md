# Generador de propuestas con IA: de 4 horas a 30 minutos por propuesta usando NeuroCore

**Categoría:** #operaciones
**Fecha:** 2026-03-17 03:04
**Impacto:** alto
**Estado:** pendiente

## Descripción

Cada propuesta comercial consume 3-4h de Andre o un senior del equipo. Con las propuestas ganadoras anteriores como base, un agente interno de IA genera el 80% del borrador en minutos a partir de las notas del discovery call. Con 2-3 propuestas por semana, son 6-9h semanales recuperadas — tiempo directo que se convierte en más reuniones, más cierre y menos dependencia de Andre en el proceso comercial.

## Cómo Ejecutar

1. Recopilar las últimas 8-10 propuestas cerradas (ganadoras y perdidas). Extraer la estructura común y crear una plantilla maestra en Notion/Google Docs con variables: [EMPRESA], [SECTOR], [PROCESO], [DOLOR_PRINCIPAL], [HORAS_PERDIDAS], [PRECIO], [CRONOGRAMA]. Es el 'molde' que el agente llenará.
2. Construir en n8n o Make un flujo de 2 pasos: Andre completa formulario de 10 campos post-discovery (empresa, sector, proceso identificado, dolor, usuarios, urgencia, precio señalado) → el agente llama a la API de Claude con la plantilla + contexto del formulario + ejemplos anteriores → genera borrador en Google Docs en menos de 5 minutos.
3. Andre revisa y ajusta el borrador (15-20 min) en lugar de escribirlo desde cero. Probar en la próxima propuesta esta semana y medir tiempo real ahorrado. Si funciona, extender para generar también el Reporte de Diagnóstico Digital automáticamente post-discovery.

## Ideas Relacionadas

- [[Sales playbook por vertical kit de ventas estandarizado para cerrar sin improvis]]
- [[Modelo de retainer mensual post-proyecto para generar MRR predecible]]
- [[Demo environment live por vertical cierra sin improvisar, delega sin riesgo]]
- [[Deal Rescue automático n8n detecta deals calientes sin actividad y genera el men]]
- [[Secuencia automática post-firma de la firma al upsell en 30 días sin esfuerzo ma]]