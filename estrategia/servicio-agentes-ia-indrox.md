# Servicio: Instalación de Agentes IA para Empresas
*Investigado: 2026-03-20 | Frieren*

## Contexto del mercado Perú
- 95% de peruanos con smartphone usan WhatsApp → canal central de cualquier bot
- Ley 31814 (primera ley de IA en LATAM, en vigor enero 2026) → legitimidad institucional
- 75% de PYMEs peruanas ya usan herramientas digitales (INEI 2025)
- Perú proyecta 3.9x multiplicador de inversión en IA, el mayor de LATAM
- Gap de mercado: entre SaaS DIY ($40–150/mes) y consultoras enterprise ($4K+ setup) hay zona casi vacía

## Competidores en Perú/LATAM
| Proveedor | Setup | Mensual | Notas |
|---|---|---|---|
| AM Software (Arequipa) | $3.9K–$7.8K | — | WhatsApp API custom dev |
| Plazbot AI | Bajo/0 | $40–$135 | Self-serve SaaS |
| CreatorsLatam | Por proyecto | Retainer opcional | Kommo + BotPress |
| WATI | — | $49–$199 | Plataforma WhatsApp SaaS |
| Kommo CRM | — | $15–45/usuario | CRM + WhatsApp, muy popular LATAM |

**El segmento $400–700 setup + $150–300/mes "done-for-you" está casi vacío en Perú.**

## Modelo de precios recomendado

### 🥉 STARTER — $499 setup / $149/mes
- Canal: WhatsApp Business API
- Bot FAQ entrenado en 1 documento (50 Q&A)
- Captura de leads → Google Sheets
- Handoff a humano
- Hasta 1,000 conversaciones/mes
- 2 semanas de ajustes post-lanzamiento

### 🥈 PRO (target principal) — $799 setup / $299/mes
- 3 canales: WhatsApp + Instagram DM + web chat
- IA con personalidad customizada (Claude/OpenAI)
- Entrenada en documentación de la empresa
- Integración CRM (Kommo o HubSpot Starter)
- Agendamiento (Google Calendar / Calendly)
- Flujo de calificación de leads
- Llamada mensual de revisión + optimizaciones
- Reporte mensual de performance

### 🥇 BUSINESS — $1,499 setup / $599/mes
- Todos los canales + email + Facebook
- IA entrenada en base de conocimiento completa
- CRM full (Kommo Pro / HubSpot / Zoho)
- Integración pagos (alertas Yape/Plin, PagoEfectivo)
- Routing multi-departamento
- Dashboard analytics (Looker Studio)
- SLA 4 horas, soporte prioritario
- Reentrenamiento trimestral
- 3 asientos de agente humano

### Add-ons
- Canal extra: +$150 setup / +$50/mes
- Migración CRM: $300 one-time
- Voice bot: $500 setup / +$150/mes
- Reentrenamiento IA: $200/sesión
- Taller de capacitación staff (2h): $250

## Stack tecnológico
- **Backbone IA:** Claude API (recomendado) o OpenAI GPT-4o
- **Automatización:** n8n / Make
- **CRM:** Kommo (mejor LATAM) o HubSpot
- **WhatsApp:** WATI o Kommo
- **Reporting:** Google Looker Studio / Notion
- **Perú-específico:** Yape/Plin alerts, PagoEfectivo, Calendly en español

## Sectores con mayor propensión de compra
1. **Clínicas / Dentistas / Estética** — citas saturadas, alto no-show
2. **Inmobiliarias** — leads 24/7, respuesta lenta = venta perdida
3. **E-commerce / retail** — consultas fuera de horario
4. **Restaurantes / catering** — reservas y carta
5. **Estudios legales / contables** — consultas de primer filtro
6. **Educación (institutos)** — matrícula y horarios
7. **Automotriz** — agendamiento de servicio técnico
8. **Turismo / agencias de viaje** — cotizaciones fuera de horario

## Proyección MRR
| Escenario | MRR |
|---|---|
| Conservador (5+8+2 clientes) | $4,335/mes |
| Moderado (10+20+5) | $10,465/mes |
| Optimista año 2 (15+35+10) | $18,690/mes |

## Pitch para vender mañana mismo
"Tu equipo responde 80 mensajes de WhatsApp al día a mano. Te instalamos un asistente que responde al instante, captura leads, agenda citas y te pasa solo los que están listos para comprar. $499 de instalación, $299 al mes. Retorno en la primera semana."
