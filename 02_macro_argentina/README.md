# 🇦🇷 Dashboard Macro Argentina

[![View Dashboard](https://img.shields.io/badge/View-Dashboard-green?style=for-the-badge)](../02_macro_argentina.html)

Dashboard interactivo de indicadores económicos argentinos con visualizaciones profesionales en dark mode.

## 📊 Indicadores Monitoreados

### Tipo de Cambio
| Tipo | Descripción |
|------|-------------|
| **Oficial** | Cotización BNA |
| **Blue** | Mercado paralelo |
| **MEP** | Dólar bolsa (AL30) |
| **CCL** | Contado con liquidación |
| **Tarjeta** | Oficial + 30% impuestos |

### Inflación
- IPC General (mensual)
- IPC Núcleo
- Inflación acumulada
- Inflación anualizada (proyección)

### Tasas de Interés
- Plazo Fijo (TNA/TEA)
- BADLAR
- Tasa de Política Monetaria
- LECAP
- Tasa Real

## 🔗 Fuentes de Datos

| Fuente | API | Datos |
|--------|-----|-------|
| [dolarapi.com](https://dolarapi.com) | REST | Cotizaciones en tiempo real |
| [bluelytics.com.ar](https://bluelytics.com.ar) | REST | Serie histórica blue |
| BCRA | - | Tasas de interés |
| INDEC | - | Inflación oficial |

## 🎨 Features del Dashboard

- ✅ **KPIs interactivos** con variaciones mensuales
- ✅ **Range slider** para zoom temporal
- ✅ **Zonas de riesgo** coloreadas (brecha cambiaria)
- ✅ **Barras dinámicas** por nivel de inflación
- ✅ **Dark mode** profesional
- ✅ **Responsive** design

## 🛠️ Tech Stack

```python
import pandas as pd
import requests
import plotly.graph_objects as go
from plotly.subplots import make_subplots
```

## 📁 Estructura

```
02_macro_argentina/
├── README.md
└── notebooks/
    └── dashboard_macro.ipynb
```

## 🚀 Ejecutar

```bash
cd 02_macro_argentina
jupyter notebook notebooks/dashboard_macro.ipynb
```

## 📈 Contexto Económico (2024)

- **Brecha cambiaria:** Comprimida de 150%+ a ~13%
- **Inflación mensual:** Reducción de 25.5% (dic-23) a 2.7% (dic-24)
- **Crawling peg:** 2% mensual de devaluación oficial
- **Tasas reales:** Positivas por primera vez en años

## 📤 Exportación

El notebook genera `dashboard_macro_argentina.html` que puede abrirse en cualquier browser sin dependencias.

---

[← Volver al Portfolio](../README.md)
