# 📊 RappiPlus — Diagnóstico Estratégico Integral

> **Proyecto Final · TripleTen Data Analytics**

---

## 🇲🇽 Español

### 📌 Descripción del proyecto

Análisis end-to-end del servicio de suscripción **RappiPlus**, con el objetivo de responder preguntas clave de negocio a partir de datos reales de pedidos, catálogo y marketing.

El proyecto cubre el ciclo completo de análisis de datos:
limpieza → rentabilidad → conversión → retención → experimentación → comunicación visual.

---

### ❓ Preguntas de negocio respondidas

| # | Pregunta | Herramienta |
|---|---|---|
| 1 | ¿Podemos confiar en los datos? | Python |
| 2 | ¿El negocio es rentable? | Python |
| 3 | ¿Dónde se pierden los usuarios? | SQL |
| 4 | ¿Los usuarios regresan? | SQL |
| 5 | ¿Los cambios generan impacto? | Python |
| 6 | ¿Cómo comunicamos los resultados? | Power BI |

---

### 🗂️ Estructura del proyecto

```
rappiplus-analysis/
│
├── data/
│   ├── orders_clean.csv          # Pedidos limpios
│   ├── catalog_clean.csv         # Catálogo de productos limpio
│   └── marketing_clean.csv       # Gasto de marketing limpio
│
├── notebook/
│   └── rappiplus_analysis.ipynb  # Notebook principal con todo el análisis
│
├── dashboard/
│   └── rappiplus_dashboard.pbix  # Dashboard en Power BI
│
└── README.md
```

---

### 🔍 Resumen de hallazgos

#### Paso 1 — Calidad de datos
- Se limpiaron **3 datasets** eliminando nulos (<2%), duplicados y valores inconsistentes
- Los datasets limpios tienen **24,600 pedidos**, **7 productos** y **1,521 registros de marketing**

#### Paso 2 — Rentabilidad
- **Revenue total:** $51.8M con una ganancia neta de $6.1M (**margen neto 11.7%**)
- El costo de productos representa el **83% del revenue** → margen ajustado
- **Electrónica** domina en volumen pero tiene el margen más bajo (10.8%)
- **Hogar y Moda** son más eficientes con márgenes del 62.5% y 59.3%
- **Laptop-Gaming-16GB** representa el 83% del revenue total → alta dependencia

#### Paso 3 — Funnel de conversión
- Conversión global del **80%** (first_visit → purchase)
- Mayor drop-off en **add_payment_info** con 13.3% de abandono
- Una vez que el usuario ingresa su pago, compra en el **99.8%** de los casos

#### Paso 4 — Retención por cohortes
- Retención semanal **consistente entre 40-44%** en todas las cohortes
- No hay caídas bruscas entre semanas → base de usuarios estable
- El **58% restante** representa una oportunidad de reactivación

#### Paso 5 — Prueba A/B
- Se evaluó un cambio en la UI del checkout
- Tasa control: **15.69%** vs Tasa tratamiento: **16.29%**
- **P-value: 0.4161** → No se rechaza H0
- El cambio **no tiene impacto estadísticamente significativo**

#### Paso 6 — Dashboard
- Dashboard ejecutivo en Power BI con KPIs, tendencias y drill-through por producto
- Filtros por fecha, categoría y país

---

### 🛠️ Tecnologías utilizadas

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-lightblue?logo=pandas)
![SQL](https://img.shields.io/badge/SQL-PostgreSQL-336791?logo=postgresql)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi)
![SciPy](https://img.shields.io/badge/SciPy-Stats-8CAAE6?logo=scipy)

| Herramienta | Uso |
|---|---|
| Python (Pandas, NumPy) | Limpieza de datos y KPIs |
| Matplotlib / Seaborn | Visualizaciones en notebook |
| SQL (PostgreSQL) | Funnel y cohortes |
| SciPy / Statsmodels | Prueba A/B (Z-test) |
| Power BI | Dashboard ejecutivo |

---

### 📈 KPIs principales

| KPI | Valor |
|---|---|
| Revenue Total | $51,836,375 |
| Profit Total | $8,757,696 |
| Gasto Marketing | $2,694,664 |
| Ganancia Neta | $6,063,032 |
| Margen Bruto | 16.9% |
| Margen Neto | 11.7% |
| Ticket Promedio | $2,107 |
| Conversión global | 80% |
| Retención semanal promedio | ~42% |

---

### 🚀 Cómo ejecutar el proyecto

1. Clona el repositorio:
```bash
git clone https://github.com/tu-usuario/rappiplus-analysis.git
```

2. Instala las dependencias:
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels sqlalchemy
```

3. Abre el notebook:
```bash
jupyter notebook notebook/rappiplus_analysis.ipynb
```

4. Para el dashboard, abre `dashboard/rappiplus_dashboard.pbix` en Power BI Desktop.

---

### 👤 Autor

Proyecto desarrollado como parte del programa de **Data Analytics de TripleTen**.

---
---

## 🇺🇸 English

### 📌 Project Description

End-to-end analysis of the **RappiPlus** subscription service, aimed at answering key business questions using real data from orders, product catalog, and marketing spend.

The project covers the full data analytics cycle:
cleaning → profitability → conversion → retention → experimentation → visual communication.

---

### ❓ Business Questions Answered

| # | Question | Tool |
|---|---|---|
| 1 | Can we trust the data? | Python |
| 2 | Is the business profitable? | Python |
| 3 | Where do users drop off? | SQL |
| 4 | Do users come back? | SQL |
| 5 | Do changes generate impact? | Python |
| 6 | How do we communicate results? | Power BI |

---

### 🗂️ Project Structure

```
rappiplus-analysis/
│
├── data/
│   ├── orders_clean.csv          # Cleaned orders data
│   ├── catalog_clean.csv         # Cleaned product catalog
│   └── marketing_clean.csv       # Cleaned marketing spend
│
├── notebook/
│   └── rappiplus_analysis.ipynb  # Main notebook with full analysis
│
├── dashboard/
│   └── rappiplus_dashboard.pbix  # Power BI dashboard
│
└── README.md
```

---

### 🔍 Key Findings Summary

#### Step 1 — Data Quality
- Cleaned **3 datasets** by removing nulls (<2%), duplicates, and inconsistencies
- Clean datasets contain **24,600 orders**, **7 products**, and **1,521 marketing records**

#### Step 2 — Profitability
- **Total Revenue:** $51.8M with a net profit of $6.1M (**11.7% net margin**)
- Product costs account for **83% of revenue** → tight margin
- **Electronics** dominates in volume but has the lowest margin (10.8%)
- **Home & Fashion** are more efficient with margins of 62.5% and 59.3%
- **Laptop-Gaming-16GB** accounts for 83% of total revenue → high dependency risk

#### Step 3 — Conversion Funnel
- Overall conversion rate of **80%** (first_visit → purchase)
- Largest drop-off at **add_payment_info** with 13.3% abandonment
- Once users enter payment info, they complete the purchase **99.8%** of the time

#### Step 4 — Cohort Retention
- Weekly retention **consistently between 40-44%** across all cohorts
- No sharp drops between weeks → stable user base
- The remaining **58%** represents a reactivation opportunity

#### Step 5 — A/B Test
- Evaluated a UI change in the checkout flow
- Control rate: **15.69%** vs Treatment rate: **16.29%**
- **P-value: 0.4161** → Fail to reject H0
- The change has **no statistically significant impact**

#### Step 6 — Dashboard
- Executive Power BI dashboard with KPIs, trends, and product drill-through
- Filters by date, category, and country

---

### 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-lightblue?logo=pandas)
![SQL](https://img.shields.io/badge/SQL-PostgreSQL-336791?logo=postgresql)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi)
![SciPy](https://img.shields.io/badge/SciPy-Stats-8CAAE6?logo=scipy)

| Tool | Usage |
|---|---|
| Python (Pandas, NumPy) | Data cleaning and KPIs |
| Matplotlib / Seaborn | Notebook visualizations |
| SQL (PostgreSQL) | Funnel and cohort analysis |
| SciPy / Statsmodels | A/B Test (Z-test) |
| Power BI | Executive dashboard |

---

### 📈 Main KPIs

| KPI | Value |
|---|---|
| Total Revenue | $51,836,375 |
| Total Profit | $8,757,696 |
| Marketing Spend | $2,694,664 |
| Net Profit | $6,063,032 |
| Gross Margin | 16.9% |
| Net Margin | 11.7% |
| Average Ticket | $2,107 |
| Global Conversion | 80% |
| Avg Weekly Retention | ~42% |

---

### 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/your-username/rappiplus-analysis.git
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels sqlalchemy
```

3. Open the notebook:
```bash
jupyter notebook notebook/rappiplus_analysis.ipynb
```

4. For the dashboard, open `dashboard/rappiplus_dashboard.pbix` in Power BI Desktop.

---

### 👤 Author

Project developed as part of the **TripleTen Data Analytics** program.
