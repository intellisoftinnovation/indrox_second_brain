---
tags: [operaciones, ia, propuestas, n8n, aceptado]
estado: "✅ Aceptado"
aprobado: 2026-03-20
idea: "[[ideas/Generador de propuestas con IA de 4 horas a 30 minutos por propuesta usando Neur]]"
---

# ⚡ Generador de Propuestas con IA
*De 4 horas → 30 minutos por propuesta*

**Por qué:** Con 2–3 propuestas/semana, Indrox pierde 6–9h semanales de tiempo senior. Este flujo recupera ese tiempo directamente en capacidad comercial.

---

## Arquitectura del flujo

```
Andre completa formulario post-discovery (10 campos, 5 min)
         ↓
n8n / Make recibe el formulario
         ↓
Llama a Claude API con: plantilla maestra + contexto del formulario + ejemplos de propuestas ganadoras
         ↓
Genera borrador en Google Docs (< 5 min)
         ↓
Andre revisa y ajusta (15–20 min)
         ↓
Exporta a PDF o envía como Loom
```

---

## Formulario de discovery (10 campos)

| Campo | Ejemplo |
|-------|---------|
| Empresa | Constructora XYZ |
| Sector | Construcción |
| Proceso identificado | Control de avance de obra |
| Dolor principal | Sobrecostos por falta de visibilidad en tiempo real |
| Usuarios del sistema | 5 ingenieros residentes + 1 gerente |
| Urgencia del cliente | Alta — proyecto en marcha |
| Precio señalado | $20K–$25K |
| Cronograma esperado | 6 semanas |
| Competidores mencionados | Ninguno |
| Notas del discovery | Quieren app móvil para ingenieros en campo |

---

## Plantilla maestra (estructura)

1. Resumen ejecutivo (1 párrafo personalizado)
2. El problema que identificamos (palabras del cliente)
3. Nuestra solución propuesta (con módulos específicos)
4. Cómo lo implementamos (cronograma en semanas)
5. Por qué Indrox (prueba social del mismo sector)
6. Inversión (precio + modelo de pago)
7. Próximos pasos (CTA concreto)

---

## Pasos para construir esto

- [ ] Recopilar 8–10 propuestas anteriores ganadoras y perdidas
- [ ] Extraer estructura común → crear plantilla maestra en Google Docs
- [ ] Crear formulario de discovery en Typeform o Google Forms (10 campos)
- [ ] Construir flujo en n8n: formulario → Claude API → Google Docs
- [ ] Probar con la próxima propuesta real
- [ ] Medir tiempo antes vs después

---

## Extensión futura
Una vez funcionando para propuestas, extender para generar:
- Reporte de Diagnóstico Digital post-discovery
- Follow-up emails personalizados post-propuesta
- Resumen de reunión con próximos pasos automático
