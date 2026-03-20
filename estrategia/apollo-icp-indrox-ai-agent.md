# Apollo ICP — Indrox AI Agent
*Creado: 2026-03-20 | Frieren*

## Filtros de búsqueda en Apollo (People)

### Títulos (is any of)
```
CEO, Gerente General, Director General, Dueño, Fundador, Propietario,
Director de Operaciones, COO, Chief Operating Officer,
Gerente de Operaciones, Presidente Ejecutivo
```
*Activar "fuzzy match" para capturar variantes como "Gte. General"*

### Seniority (is any of)
```
C-Suite / Owner / Director
```

### Ubicación
```
País: Peru
Ciudades: Lima, Lima Metropolitan Area, Miraflores, San Isidro,
          Santiago de Surco, Arequipa, Trujillo
```

### Email Status
```
✅ Verified
✅ Likely to engage
❌ Excluir: Unverified / Catch-all only
```

---

## Filtros de empresa (Company)

### Headcount
```
Mínimo: 10 | Máximo: 150
Sweet spot: 25–80 empleados
```

### Industrias (is any of)
```
Management Consulting, Professional Services, Import and Export,
Construction, Marketing and Advertising, Hospital & Health Care,
Education Management, Real Estate, Accounting, Staffing and Recruiting
```

### Excluir industrias
```
Government Administration, Mining & Metals, Oil & Energy,
Computer Software, Internet, Venture Capital & Private Equity
```

### Tecnologías usadas (filtro de calidad — requiere Apollo Enrichment)
```
✅ Google Workspace / Gmail
✅ HubSpot
✅ Slack
✅ QuickBooks
✅ Zoom
✅ Notion
```
*Estas señales = ejecutivo digitalmente maduro, listo para adoptar IA*

### Keywords de empresa
```
"empresa peruana", "servicios profesionales", "importadora",
"exportadora", "inmobiliaria", "clínica", "colegio particular",
"agencia de marketing", "contabilidad", "consultoría"
```

---

## Criterios de priorización

### 🔴 HOT — Trabajar primero
- Usa Google Workspace + HubSpot + Slack juntos
- 25–80 empleados
- LinkedIn activo (post en últimos 30 días)
- Industria: Consultoría, Agencia Marketing, Import/Export
- Lima (Miraflores, San Isidro, Surco)
- Título: Fundador / Dueño (no burocracia, puede firmar esta semana)
- Email verificado
- Empresa fundada 2015–2022

### 🟡 WARM — Nurture
- Solo Google Workspace (sin HubSpot/Slack)
- 80–150 empleados
- Director de Operaciones (influencer, no decisor)
- Arequipa / Trujillo

### 🔵 SKIP
- 150+ empleados
- Sin tech stack identificable
- Email catch-all solamente
- Título: Coordinador, Supervisor, Jefe de área
- Minería, Gobierno, retail masivo

---

## Mensajes de outreach (listos para usar)

### A. Solicitud de conexión LinkedIn (≤300 chars)
```
Hola [Nombre], vi que lideras [Empresa] — trabajo con gerentes generales 
de empresas como la tuya en Lima. Tengo algo específico que te puede 
ahorrar tiempo real. ¿Conecto?
```

*Variante para consultoras:*
```
Hola [Nombre], trabajo con dueños de consultoras en Lima que perdían 
2–3 horas al día en reportes y seguimiento. Ahora lo automatizan. 
¿Conversamos?
```

### B. Primer mensaje post-conexión (≤500 chars)
```
[Nombre], gracias por conectar.

Directo al punto: construimos un asistente de IA interno para gerentes 
generales de empresas de 20–100 personas en Lima.

Lo que resuelve: el briefing diario que hoy armas tú solo, el seguimiento 
de cobranzas que se pierde en WhatsApp, y saber tu flujo de caja sin 
tener que llamar a tu contador.

¿Tienes 20 minutos esta semana para ver si aplica a [Empresa]?
```

*Variante si usan HubSpot:*
```
[Nombre], gracias por aceptar.

Veo que en [Empresa] usan HubSpot — eso me dice que ya tienen procesos 
digitales. El problema que resolvemos es el siguiente nivel: que tú como 
gerente no tengas que perseguir a tu equipo para saber qué pasó ayer.

Indrox AI Agent te da ese briefing solo, cada mañana.

¿15 minutos esta semana?
```

### C. Seguimiento sin respuesta (≤400 chars)
```
[Nombre], entiendo que estás ocupado — de hecho, ese es exactamente 
el problema que resolvemos.

Una sola pregunta: ¿cuántas horas a la semana pierdes en WhatsApp 
tratando de saber el estado de tu equipo o tus cobros?

Si es más de 3, vale que hablemos 15 minutos. Si no, no te molesto más.
```

*Variante SUNAT para contadores/importadoras:*
```
[Nombre], última vez que escribo.

Muchos gerentes con los que hablamos perdían tiempo real revisando 
manualmente si tenían multas o alertas de SUNAT. Ahora lo tienen 
automatizado.

¿Vale 15 minutos ver si tiene sentido para [Empresa]? Si no, sin problema.
```

---

## Secuencia Apollo (5 toques)

| Paso | Día | Canal | Acción |
|---|---|---|---|
| 1 | 0 | LinkedIn | Solicitud de conexión (Template A) |
| 2 | 2 | LinkedIn | Primer mensaje si aceptó (Template B) |
| 3 | 5 | Email | Cold email mismo ángulo que B |
| 4 | 9 | LinkedIn/Email | Follow-up (Template C) — canal donde no respondió |
| 5 | 14 | Email | Breakup: "Cerrando este hilo — si en algún momento tiene sentido, aquí estoy." |

### Email Step 3

**Subject:** `¿Cuánto tiempo pierde tu equipo en reportes, [Nombre]?`

```
Hola [Nombre],

Trabajo con gerentes generales de empresas de servicios en Lima 
(20–100 personas) que enfrentan el mismo problema:

→ El día empieza revisando WhatsApp para saber qué pasó ayer
→ El flujo de caja lo saben cuando llaman al contador
→ El seguimiento de cobranzas depende de que alguien se acuerde

Construimos Indrox AI Agent — un asistente interno que centraliza 
todo eso y te da un briefing diario automatizado.

No es un chatbot de atención al cliente. Es para ti, como gerente.

¿Tienes 15 minutos esta semana para ver si aplica a [Empresa]?

[Tu nombre]
Indrox
```

---

## Configuración técnica Apollo

```
Tipo de secuencia:   Linear
Ventana de envío:    Lun–Jue, 8:00am–12:00pm (America/Lima)
Cap diario:          40–60 emails/día (protege reputación del dominio)
Auto-skip fines:     SÍ
Stop trigger:        Respuesta recibida OR reunión agendada
From name:           [Tu nombre] — NO "Indrox Team"
Dominio envío:       outreach.indrox.pe (subdominio, protege indrox.pe)
```

## Checklist de arranque
```
[ ] Apollo con email + LinkedIn steps habilitados (Basic+ o superior)
[ ] Importar filtros → guardar como "ICP-Peru-GerGen"
[ ] Crear secuencia "ICP-Peru-GerGen-5Touch"
[ ] Warm-up del dominio outreach.indrox.pe (2 semanas antes de blast)
[ ] Construir lista de 200 leads verificados antes de lanzar
[ ] Taggear: ICP-Hot / ICP-Warm / ICP-Cold
[ ] Métricas objetivo: Open rate >40% | Reply rate >4%
[ ] A/B test de subject lines después de 100 envíos
```

## Nota estratégica clave
> El filtro más fuerte no es la industria — es **tech stack + tamaño + título**.
> Una agencia de marketing de 40 personas en Miraflores con HubSpot y Google Workspace 
> tiene 5x más probabilidad de convertir que una constructora de 100 personas sin tech identificable.
> Correr primero las listas filtradas por tecnología.
