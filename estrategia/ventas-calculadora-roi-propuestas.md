---
tags: [ventas, roi, calculadora, propuesta, aceptado]
estado: "✅ Aceptado"
aprobado: 2026-03-20
idea: "[[ideas/Calculadora de ROI embebida en propuestas cifras del cliente, no tuyas]]"
---

# 🧮 Calculadora ROI en Propuestas (Cifras del Cliente)
*Esta semana · Costo: $0*

**Por qué:** El número lo construye el cliente — es irrefutable. Elimina la objeción "no sé si vale la pena" antes de que la digan.

---

## Estructura de la hoja (Google Sheets)

### Tab 1 — Inputs del cliente

| Campo | Ejemplo | Lo llena |
|-------|---------|---------|
| Proceso a automatizar | Control de avance de obra | Cliente |
| Horas semanales del equipo en ese proceso | 15h | Cliente |
| Costo hora promedio del equipo (USD) | $8 | Cliente |
| Número de errores manuales por mes | 12 | Cliente |
| Costo promedio de cada error (USD) | $200 | Cliente |
| Frecuencia de reportes manuales (horas/mes) | 20h | Cliente |

### Tab 2 — Resultados automáticos

| Métrica | Fórmula | Resultado ejemplo |
|---------|---------|-----------------|
| Ahorro anual en horas | `(horas_sem × 0.7) × 52 × costo_hora` | $4,368/año |
| Ahorro por eliminación de errores | `errores_mes × 12 × costo_error × 0.8` | $23,040/año |
| Ahorro total proyectado | Suma | $27,408/año |
| Inversión Indrox | (precio del proyecto) | $20,000 |
| Payback | `inversión / (ahorro_anual / 12)` | 8.7 meses |
| ROI año 1 | `(ahorro - inversión) / inversión × 100` | 37% |
| ROI año 2 | `ahorro × 2 / inversión × 100` | 174% |

---

## Cómo integrarlo al proceso de venta

**Antes de enviar la propuesta:**
> *"Antes de prepararte la propuesta formal, llenemos esto juntos en 5 min — necesito tus números reales para que el proyecto tenga sentido financiero para ti."*

Andre comparte el link al Google Sheet (modo "comment only" — el cliente solo escribe en las celdas azules).

El cliente llena sus propios números → ve que el ROI es real → la propuesta formal llega con los números ya validados por él mismo.

---

## Pasos inmediatos

- [ ] Crear el Google Sheet con la estructura de arriba
- [ ] Proteger las fórmulas (solo editable las celdas de input)
- [ ] Probar con 3 propuestas activas esta semana
- [ ] Ajustar fórmulas si los sectores tienen variables distintas (logística vs construcción vs minería)

---

## Nota
Esta calculadora es diferente a la de lead magnet público. Esa es para captación. Esta es para el proceso de cierre — más detallada, con los números reales del cliente, usada en la fase de propuesta.
