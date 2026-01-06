# 🎯 Credit Scoring Model

[![View Dashboard](https://img.shields.io/badge/View-Dashboard-red?style=for-the-badge)](../03_credit_scoring.html)

Modelo predictivo de default crediticio usando machine learning con comparativa de algoritmos.

## 📊 Dataset

**Kaggle: "Give Me Some Credit"**

| Métrica | Valor |
|---------|-------|
| Registros | 150,000 |
| Features | 10 |
| Target | `SeriousDlqin2yrs` |
| Default Rate | 6.7% |
| Train/Test Split | 80/20 |

## 🔧 Features Utilizadas

| Feature | Descripción | Importancia |
|---------|-------------|-------------|
| `RevolvingUtilization` | Uso de línea de crédito | 28% |
| `TotalLateTimes` | Suma de moras (30-89 días) | 19% |
| `DebtRatio` | Ratio deuda/ingreso | 14% |
| `age` | Edad del cliente | 12% |
| `NumberOfOpenCreditLines` | Líneas de crédito abiertas | 9% |
| `MonthlyIncome` | Ingreso mensual | 7% |
| `NumberRealEstateLoans` | Préstamos hipotecarios | 5% |

## 🤖 Modelos Comparados

| Modelo | AUC-ROC | Gini | KS | F1-Score |
|--------|---------|------|-----|----------|
| Logistic Regression | 0.823 | 0.646 | 0.487 | 0.217 |
| **Random Forest** | **0.867** | **0.734** | **0.583** | **0.235** |
| XGBoost | 0.854 | 0.708 | 0.551 | 0.228 |

### 🏆 Mejor Modelo: Random Forest

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=100,
    max_depth=12,
    min_samples_split=10,
    class_weight='balanced',
    random_state=42,
    n_jobs=-1
)
```

## 📈 Métricas de Evaluación

| Métrica | Valor | Descripción |
|---------|-------|-------------|
| **AUC-ROC** | 0.867 | Área bajo curva ROC |
| **Gini** | 0.734 | 2×AUC - 1 |
| **KS Statistic** | 0.583 | Máxima separación de distribuciones |
| **Precision** | 0.142 | TP / (TP + FP) |
| **Recall** | 0.685 | TP / (TP + FN) |

## 🛠️ Tech Stack

```python
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import roc_auc_score, roc_curve
import xgboost as xgb
import plotly.graph_objects as go
```

## 📁 Estructura

```
03_credit_scoring/
├── README.md
└── notebooks/
    └── credit_model.ipynb
```

## 🚀 Ejecutar

```bash
cd 03_credit_scoring
jupyter notebook notebooks/credit_model.ipynb
```

## 💡 Key Findings

1. **Random Forest** supera a Logistic Regression en +5.3% AUC
2. **RevolvingUtilization** es el predictor más importante (28%)
3. **class_weight='balanced'** mejora significativamente el recall
4. Threshold óptimo: **0.35** (maximiza F1-Score)
5. El modelo captura 58% de defaults en el top 20% de scores

## 💼 Business Impact

- Reducción estimada del **40%** en pérdidas crediticias
- Filtrado efectivo del decile más riesgoso
- Automatización del proceso de scoring

---

[← Volver al Portfolio](../README.md)
