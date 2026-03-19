# Microproducto self-serve: Auditoría Express de Procesos a $299 sin llamada de ventas

**Categoría:** #producto
**Fecha:** 2026-03-17 03:14
**Impacto:** alto
**Estado:** pendiente

## Descripción

Una página de pago simple (Stripe + Typeform) donde cualquier empresa compra por $299 una auditoría automatizada de sus 3 procesos más críticos: el comprador llena 15 preguntas, Indrox entrega en 48h un reporte PDF generado con IA con el costo estimado del dolor y recomendación de automatización. Convierte prospectos que no quieren llamada de ventas todavía, genera ingresos sin costo marginal de adquisición, y el que paga $299 ya demostró intención fuerte — la conversión a proyecto completo ($12-20K) de ese perfil es múltiplos mayor que un lead frío.

## Cómo Ejecutar

1. Esta semana: construir la página en Framer, Notion o una landing simple (Canva → link de Stripe). Typeform de 15 preguntas sobre proceso actual, sector, personas involucradas, frecuencia y costo hora aproximado. Stripe con precio fijo $299. Conectar ambas vía Make/n8n: al pago confirmado, el formulario se envía automáticamente a Andre + se genera borrador con Claude.
2. Construir el flujo de generación del reporte en n8n/Make: respuestas del Typeform → prompt a Claude → genera reporte de 3 páginas en el formato de Diagnóstico Digital ya existente (reusar la plantilla) → exportar a PDF vía Google Docs o Gamma → enviar al cliente en 48h por email. El 80% del trabajo lo hace la IA; Andre revisa en 20 min.
3. Publicar el producto en LinkedIn con post de Andre: 'Lanzamos una auditoría express de procesos por $299 — sin llamadas, sin compromiso. En 48h te decimos cuánto te está costando tu operación manual y qué automatizar primero. Link en comentarios.' También incluirlo como CTA alternativo en outreach a quienes no responden a la propuesta de diagnóstico gratuito.

## Ideas Relacionadas

- [[Piloto de 2 semanas a precio fijo como oferta de entrada sin fricción]]
- [[Templates gratuitos en Maken8n como canal de inbound calificado]]
- [[ROI tracker in-app cada sistema muestra en tiempo real cuánto valor ha generado ]]
- [[Reporte de Diagnóstico Digital post-discovery entregable brandado que vende solo]]
- [[Audit Express 48h gratuito diagnóstico de automatización para un proceso crítico]]