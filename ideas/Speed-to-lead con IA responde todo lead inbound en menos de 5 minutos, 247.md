# Speed-to-lead con IA: responde todo lead inbound en menos de 5 minutos, 24/7

**Categoría:** #ventas
**Fecha:** 2026-03-17 04:44
**Impacto:** alto
**Estado:** pendiente

## Descripción

Investigaciones muestran que el primer proveedor en responder a un lead tiene 78% más probabilidad de cerrar. Hoy los leads del diagnóstico gratuito, la calculadora y el mini-curso esperan respuesta manual de Andre. Con n8n + Claude, Indrox responde automáticamente en menos de 5 min con mensaje personalizado al sector del prospecto + link de Calendly. Es ventaja compuesta: Indrox llega primero mientras el competidor ni se enteró.

## Cómo Ejecutar

1. Construir flujo en n8n: trigger al recibir nuevo submission en Typeform (calculadora, diagnóstico, mini-curso) → extraer sector y pain del formulario → llamada a API de Claude con prompt 'genera respuesta cálida de 4 líneas personalizada al sector [X] y dolor [Y] de Indrox, incluye link de Calendly al final' → enviar por email inmediatamente. Configurar en menos de 2h esta semana.
2. Redactar los 3-4 prompts base (uno por sector: construcción, logística, minería, genérico) con el tono de Andre — revisar 5 respuestas generadas antes de activar en producción para asegurarse que suenan auténticas, no robóticas.
3. Activar y medir durante 2 semanas: comparar tasa de agendamiento de leads que reciben respuesta en <5 min vs los históricos con respuesta en horas. Meta: subir el rate de lead→reunión agendada de lo que sea que esté hoy a +30%. Si el resultado lo justifica, extender a WhatsApp con Twilio o Meta Business API.

## Ideas Relacionadas

- [[Secuencia outbound para COOs de empresas logísticas en Lima]]
- [[Outreach LinkedIn para constructoras partes de campo digitales como entrada]]
- [[Campaña de reactivación de leads fríos con 'novedad' como gancho]]
- [[Invitar prospectos top al podcast HiddenLayer como guests]]
- [[Campaña de upsell a clientes actuales con propuesta 'siguiente paso' de NeuroCor]]