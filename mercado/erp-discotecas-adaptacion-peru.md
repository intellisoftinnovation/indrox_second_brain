# ERP Discotecas — Adaptación al Mercado Peruano
*Investigado: 2026-03-20 | Frieren*
*Basado en: ERP_Magma_Requerimientos_20250910_1809.xlsx*

## Resumen de cambios España → Perú

| Módulo | España (Original) | Perú (Adaptación) |
|---|---|---|
| Facturación | VeriFactu + AEAT | SUNAT CPE vía OSE/SEE |
| RRHH/Planilla | Woffu + Nomio + RGPD | Buk/Módulo propio + T-Registro/PLAME |
| Pagos | PSD2 / 3DS2 | SBS + Yape/Plin/Niubiz/Izipay/Culqi |
| Ticketera | Fourvenues | Módulo propio + integración Joinnus opcional |
| Cashless POS | Agora + SafetyGlobal | POS local + NFC/RFID + Yape QR |
| Stock/Compras | Yurest | Módulo propio (Yurest no existe en Perú) |
| Marketing | Fidelcity + RGPD | CRM propio + cumplimiento Ley 29733 |
| Privacidad | RGPD (EU) | Ley N° 29733 + DS 003-2013-JUS |

---

## MÓDULO 1: RRHH / PLANILLA

### Trabajo nocturno en Perú (crítico)
- Horario nocturno: **10:00 PM – 06:00 AM**
- Sobretasa nocturna: **+35% sobre RMV mínimo**
- Remuneración mínima nocturna: **S/ 1,383.75** (RMV S/1,025 × 1.35)
- Vacaciones: **30 días calendario al año** (no acumulación mensual)
- Gratificaciones: **julio y diciembre (1 sueldo c/u)**
- CTS: **depósito semestral mayo y noviembre**
- Horas extras: 25% primeras 2h, 35% adicionales

### Cálculos automáticos requeridos
- Aporte AFP/ONP + comisiones actualizadas SBS
- EsSalud: 9% sueldo bruto
- Renta 5ta Categoría (escalas UIT)
- Bonificación nocturna 35%
- Gratificación semestral

### Declaraciones obligatorias
- **T-Registro** (SUNAT) — alta/baja trabajadores
- **PLAME / PDT 601** (mensual) — planilla electrónica
- **AFP Net** (mensual) — por AFP del trabajador
- **Renta 5ta Categoría** (mensual, retención)

### Herramientas recomendadas (reemplaza Woffu + Nomio)
- **Buk Perú** — líder, integra T-Registro y PLAME ✅
- **GeoVictoria** — control de asistencia/turnos rotativos ✅
- **Módulo propio vía API SUNAT** — recomendado para control total

### Tipos de personal en discotecas
- **Empleados en planilla (DL 728):** barmans, seguridad, mozos
- **Artistas/DJ:** locadores de servicios (4ta categoría), recibos por honorarios, NO planilla
- **Personal eventual:** contratos temporales o service

---

## MÓDULO 2: FACTURACIÓN ELECTRÓNICA

### Reemplaza: VeriFactu → SUNAT CPE vía OSE

**Flujo técnico:**
```
[ERP/POS] → XML UBL 2.1 → [OSE] → valida → CDR (Constancia)
```
- Certificado digital X.509 obligatorio
- Formato: XML UBL 2.1
- QR obligatorio en comprobantes
- Plazo envío: mismo día o máximo 3 días

### Comprobantes para discotecas
| Comprobante | Uso |
|---|---|
| **Boleta electrónica** | Consumidor final (entrada, consumo barra) |
| **Factura electrónica** | Empresas con RUC (eventos corporativos, VIP) |
| **Nota de crédito** | Devoluciones / cancelaciones |
| **Ticket POS** | Ventas menores |

### OSE autorizados recomendados
- **Nubefact** — popular en Perú, API REST moderna ✅
- **Greenter** — open source, ideal para integración propia ✅
- EDICOM, Efact, Sefac (alternativas)

---

## MÓDULO 3: POS / CASHLESS

### Reemplaza: PSD2/3DS → SBS + ecosistema peruano

### Métodos de pago obligatorios
| Método | Prioridad |
|---|---|
| **Yape** (BCP) | 🔴 CRÍTICO — 60M+ usuarios |
| **Plin** (BBVA+Interbank) | 🔴 CRÍTICO |
| **Visa/Mastercard vía Niubiz** | 🔴 CRÍTICO |
| **Izipay** | 🔴 CRÍTICO |
| **Culqi** (pagos online/link) | 🟡 IMPORTANTE |
| Efectivo | 🔴 CRÍTICO (sigue dominando) |

### Arquitectura cashless recomendada
**Para eventos grandes:**
```
Pulsera NFC/RFID con saldo prepago
+ Recarga vía Yape/tarjeta en ingreso
+ Lector RFID en cada barra
+ ERP centralizado
```

**Sin hardware adicional:**
```
QR dinámico Yape + Niubiz POS físico = solución mínima viable
```

### POS software compatible Perú
- **Bsale** — POS + facturación electrónica SUNAT
- **PANCA POS** — F&B peruano, integra Yape/Plin
- **Módulo propio ERP** — control total (recomendado)

---

## MÓDULO 4: STOCK Y COMPRAS

### Reemplaza: Yurest → módulo propio (Yurest no tiene presencia en Perú)

**Consideraciones específicas:**
- Licencias municipales de venta de alcohol (por distrito)
- Registro de bebidas importadas/nacionales por proveedor
- Mermas de cócteles (importante para control de costos)
- Integración con guías de remisión electrónica SUNAT

---

## MÓDULO 5: TICKETS Y ACCESO

### Reemplaza: Fourvenues → módulo propio

**Ecosistema ticketera peruano:**
- **Joinnus** (adquirida por Credicorp/BCP) — segunda plataforma, cobran 8–12%
- **Teleticket** — líder eventos masivos, menos relevante para clubs
- **Passline** — tercer jugador LATAM

**Decisión arquitectural:** Indrox construyó su **propia ticketera** — no depende de Joinnus ni Teleticket. Esto elimina el 8–12% de comisión y puede venderse como **SaaS independiente** a otras discotecas/organizadores de eventos.

---

## MÓDULO 6: PRIVACIDAD DE DATOS

### Reemplaza: RGPD → Ley N° 29733

**Marco legal peruano:**
- **Ley N° 29733** — Ley de Protección de Datos Personales
- **DS 003-2013-JUS** — Reglamento
- **ANPD** — Autoridad Nacional de Protección de Datos

**Diferencias clave con RGPD:**
- Registro de bancos de datos personales ante ANPD (si aplica)
- Consentimiento expreso para marketing directo
- Derecho de acceso, rectificación y cancelación (ARCO)
- Multas menores que RGPD pero sancionables

---

## MÓDULO 7: MARKETING Y FIDELIZACIÓN

### Reemplaza: Fidelcity + Chatpion → CRM propio + canales peruanos

**Canales de marketing digital para discotecas peruanas:**
- **Instagram** — canal principal (reservas, eventos, RRPP)
- **WhatsApp Business API** — comunicación directa con clientes
- **TikTok** — creciente para promoción de eventos
- **Facebook** — secundario pero activo en segmento 30+

**Automatización recomendada:**
- n8n + WhatsApp Business API para recordatorios de eventos
- Integración con WATI o Kommo para CRM de clientes
