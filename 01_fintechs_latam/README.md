# 📈 Análisis Fintechs LATAM

[![View Dashboard](https://img.shields.io/badge/View-Dashboard-blue?style=for-the-badge)](../01_fintechs_latam.html)

Análisis comparativo de performance y valuación de las principales fintechs latinoamericanas cotizantes en NYSE/NASDAQ.

## 🏢 Empresas Analizadas

| Ticker | Empresa | País | Sector | Market Cap |
|--------|---------|------|--------|------------|
| **MELI** | MercadoLibre | 🇦🇷 Argentina | E-commerce + Fintech | $85.2B |
| **NU** | Nubank | 🇧🇷 Brasil | Digital Banking | $52.4B |
| **DLO** | DLocal | 🇺🇾 Uruguay | Payments | $4.8B |
| **STNE** | StoneCo | 🇧🇷 Brasil | Payments | $5.6B |

## 📊 Métricas Calculadas

### Performance
- Retorno total y anualizado
- Volatilidad (desviación estándar anualizada)
- Sharpe Ratio (risk-free rate: 5%)
- Sortino Ratio
- Maximum Drawdown
- Value at Risk (VaR 95%)
- Beta vs S&P 500

### Valuación
- EV/Revenue
- P/S Ratio
- Revenue Growth YoY

### Correlaciones
- Matriz de correlación de retornos diarios
- Rolling correlation (90 días)

## 🛠️ Tech Stack

```python
import pandas as pd
import numpy as np
import yfinance as yf
import plotly.express as px
import plotly.graph_objects as go
```

## 📁 Estructura

```
01_fintechs_latam/
├── README.md
└── notebooks/
    └── analisis_fintechs.ipynb
```

## 🚀 Ejecutar

```bash
cd 01_fintechs_latam
jupyter notebook notebooks/analisis_fintechs.ipynb
```

## 📈 Key Findings

- **MELI** lidera en Sharpe Ratio (0.98) - mejor retorno ajustado por riesgo
- **NU** mayor retorno absoluto (+58% YTD) pero también mayor volatilidad
- **DLO** sufrió drawdown severo (-72%) por concerns regulatorios
- Correlación promedio del sector: **0.64** (diversificación limitada)

## 📝 Fuente de Datos

- **Yahoo Finance** via `yfinance` API
- Período: Enero 2023 - Diciembre 2024
- Precios ajustados por dividendos y splits

---

[← Volver al Portfolio](../README.md)
