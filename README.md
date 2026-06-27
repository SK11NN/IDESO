# Proyecto Ernesto Investing AI

## Descripción
 
Sistema web de apoyo en decisiones de inversión bursátil desarrollado mediante el paradigma de **Programación Asistida por Inteligencia Artificial**. El sistema integra modelos predictivos de Machine Learning con visualizaciones interactivas de datos financieros reales de empresas mineras con operaciones en Perú.
 
El proyecto documenta empíricamente la efectividad del desarrollo asistido por IA, validando mediante pruebas estadísticas (t de Student) que esta metodología permite construir un DSS financiero funcional con una reducción del 76.6% en tiempo de desarrollo respecto a la programación manual.
 
---
 
## Módulos del Frontend
 
| Módulo | Archivo | Descripción |
|--------|---------|-------------|
| Inicio | `index.html` | Portal de navegación del sistema |
| Autenticación | `login.html` | Login, registro y recuperación de cuenta |
| Dashboard de Mercado | `dash_merc.html` | Velas japonesas, indicadores técnicos (SMA/EMA/RSI), volumen |
| Gestión de Portafolio | `portafolio.html` | Visualización de activos y métricas de rendimiento |
| Dashboard Integral | `Dashboard_Integral_1.html` | Vista consolidada con modelos ML y predicciones LSTM |
 
---
 
## Activos Financieros
 
Empresas mineras con operaciones en Perú, alineadas con la investigación doctoral del docente:
 
| Ticker | Empresa | Bolsa |
|--------|---------|-------|
| FSM | Fortuna Silver Mines Inc. | NYSE |
| VOLCABC1.LM | Volcan Compañía Minera S.A.A. | BVL |
| ABX.TO | Barrick Gold Corporation | TSX |
| BVN | Cía. de Minas Buenaventura S.A.A. | NYSE |
| BHP | BHP Billiton Limited | NYSE |
 
---
 
## Stack Tecnológico
 
**Frontend:** HTML5 · CSS3 · JavaScript · Plotly.js · Chart.js  
**Backend:** Python 3.12 · Google Colab · FastAPI · uvicorn · ngrok  
**Datos:** yfinance · Yahoo Finance  
**ML/DL:** scikit-learn (SVC) · TensorFlow/Keras (LSTM, BiLSTM, GRU, SimpleRNN)  
**IA utilizada:** Claude AI · ChatGPT · GitHub Copilot · Gemini
 
---
 
## Integración Frontend–Backend
 
El backend corre en Google Colab y se expone mediante un túnel ngrok:
 
```
GET /api/mercado/{ticker}   → datos OHLCV con indicadores técnicos
GET /api/svc/{ticker}       → señales y métricas del clasificador SVC
GET /api/rnns/{ticker}      → comparación de clasificadores RNN
GET /api/lstm/{ticker}      → predicciones del regresor LSTM
GET /api/salud              → health check
```
 
El archivo `dash_merc.html` consume la API en tiempo real; ante falta de conexión, cae automáticamente a datos simulados.
 
---
 
## Estructura del Repositorio
 
```
Proyecto-Ernesto-Investing-AI/
├── index.html
├── login.html
├── dash_merc.html
├── portafolio.html
├── Dashboard_Integral_1.html
├── notebooks/
│   ├── NB1_Ingesta.ipynb
│   ├── NB2_SVC.ipynb
│   ├── NB3_RNNs.ipynb
│   └── NB4_LSTM.ipynb
├── docs/
│   ├── EQ1_Borrador Artículo SPBI.docx
└── README.md
```
 
---
 
## Integrantes
 
- Caballero Maravi, Darren Esteban
- Gomez Gutierrez, David Adrian
- Oliva Rayme, Oliver Ignacio David
- Rubio Collantes, Imanol Valentino
- Sánchez Soto, Gianella Ariana Mia
- Silva Gamero, Mateo
