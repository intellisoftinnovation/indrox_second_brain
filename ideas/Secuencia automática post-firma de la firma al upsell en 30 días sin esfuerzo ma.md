# Secuencia automática post-firma: de la firma al upsell en 30 días sin esfuerzo manual

**Categoría:** #operaciones
**Fecha:** 2026-03-17 13:01
**Impacto:** alto
**Estado:** pendiente

## Descripción

Cada proyecto firmado desencadena hoy un proceso ad hoc y manual. Una secuencia de 6 mensajes automáticos (WhatsApp + email) activada el día de la firma mantiene al cliente informado, recoge NPS a mitad del proyecto y abre la conversación de upsell al día 28 — cuando el cliente ya vio resultados pero antes de que el entusiasmo baje. Reduce churn, multiplica referidos espontáneos y genera expansión con cero esfuerzo adicional de Andre.

## Cómo Ejecutar

1. Mapear 6 momentos del ciclo: Día 0 (bienvenida + qué esperar), Día 3 (check-in de accesos y datos), Día 7 (confirmar primer milestone técnico), Día 14 (pulse check de 1 pregunta: '¿Hay algo que ajustar antes de la entrega?'), Día 21 (preview de lo que se entregará), Día 28 (post-entrega: '¿Qué proceso te gustaría automatizar a continuación?'). Redactar los 6 mensajes esta semana en el tono directo de Andre — sin corporativismo.
2. Configurar en n8n: trigger manual cuando Andre cambia el estado del deal en el CRM a 'firmado' → secuencia de 6 mensajes con delays correspondientes vía WhatsApp (Twilio/Meta Business API) + email (Brevo). Variables por mensaje: nombre del cliente y nombre del proceso acordado. Tiempo de build estimado: 3-4h.
3. Activar en el próximo proyecto firmado como piloto. Medir: tasa de respuesta al pulse check del día 14 (señal de satisfacción temprana), conversiones a retainer o upsell desde el mensaje del día 28, y menciones espontáneas de la comunicación proactiva. Si funciona, activar retroactivamente en todos los proyectos activos y hacerlo parte del onboarding estándar de cada cliente nuevo.

## Ideas Relacionadas

- [[Sales playbook por vertical kit de ventas estandarizado para cerrar sin improvis]]
- [[Modelo de retainer mensual post-proyecto para generar MRR predecible]]
- [[Demo environment live por vertical cierra sin improvisar, delega sin riesgo]]
- [[Generador de propuestas con IA de 4 horas a 30 minutos por propuesta usando Neur]]
- [[Deal Rescue automático n8n detecta deals calientes sin actividad y genera el men]]