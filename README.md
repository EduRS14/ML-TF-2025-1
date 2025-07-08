# 🧠 Predicción de Tendencias en Criptomonedas con Machine Learning

## 🎯 Objetivo del trabajo

Desarrollar un modelo de aprendizaje automático capaz de anticipar si una criptomoneda tenderá a subir o bajar su precio, utilizando datos históricos de precio, capitalización de mercado (Market Cap), valor total bloqueado (TVL) y categoría temática (IA, Gaming, RWA, Meme). Este modelo busca ofrecer una herramienta de soporte a decisiones de inversión, basada en patrones detectados en el comportamiento de activos seleccionados.

---

## 👥 Integrantes

| Nombre                        | Código       |
|------------------------------|--------------|
| Alfredo Mauricio Aragón Ovalle | U202210494 |
| Tarik Gustavo Morales Oliveros | U202210472 |
| Rodrigo Alonso Ramírez Cesti   | U202210690 |
| Daniella Alexandra Vargas Saldaña | U202219211 |
| Eduardo José Rivas Siesquén     | U202216407 |

---

## 📊 Descripción del dataset

Se trabajó con datos históricos de 12 criptomonedas agrupadas en 4 categorías (IA, Gaming, RWA, Meme), recolectados desde plataformas como:

- [CoinGecko](https://www.coingecko.com)
- [DeFiLlama](https://defillama.com)
- [CoinCodex](https://coincodex.com)

Los datos incluyeron columnas como `price`, `market_cap`, `TVL`, `volume`, `open`, `high`, `low`, entre otros. Se usó un enfoque de ventanas móviles (8 semanas) y se diseñó un conjunto de características estadísticas y transformadas para modelado predictivo.

---

## 🚀 Propuesta final elegida

Tras la comparación entre distintos modelos de clasificación y regresión, se seleccionaron como enfoques más robustos:

- ✅ **Random Forest** con diferencias porcentuales como atributos, logrando un AUC promedio de ~0.91.
- ✅ **XGBoost Regressor**, que obtuvo un R² de 0.95, MAE de 0.2154 y RMSE de 0.2835.
- ✅ Complemento con **SARIMAX + GARCH** para modelar tendencias y volatilidad financiera.

Estos modelos fueron integrados en una **interfaz web interactiva** para usuarios técnicos y no técnicos.

---

## 🌐 Demo del modelo

La interfaz del modelo fue desarrollada con **Gradio** y desplegada en línea:

🔗 [Ir a la demo pública en Gradio](https://cd108eeff1abc09bf3.gradio.live/)

---

## 🔍 Conclusiones

- El análisis mostró que transformar los datos (diferencias absolutas o porcentuales) mejora significativamente la capacidad predictiva frente a los valores originales.
- Modelos como Random Forest y XGBoost demostraron mayor precisión y generalización en comparación con Prophet.
- Se evidenció que la combinación de técnicas estadísticas con modelos de ML puede ofrecer predicciones robustas en mercados volátiles.
- Se construyó una interfaz amigable y funcional que facilita la interpretación de resultados y la toma de decisiones.

---

## 📚 Trabajos relacionados

- **McNally, S., Roche, J., & Caton, S. (2018)**  
  *Predicting the price of Bitcoin using Machine Learning.*  
  *2018 26th Euromicro International Conference on Parallel, Distributed and Network-based Processing (PDP)*, 339–343.  
  [https://doi.org/10.1109/PDP2018.2018.00060](https://doi.org/10.1109/PDP2018.2018.00060)

- **Álvarez-Díaz, L. J. (2019)**  
  *Criptomonedas: Evolución, crecimiento y perspectivas del Bitcoin.*  
  *Población y desarrollo, 25(49)*, 130–142.  
  [https://hdl.handle.net/11000/28290](https://hdl.handle.net/11000/28290)

- **García Candela, O. (2022)**  
  *Cryptomonedas.*  
  Tesis de licenciatura, Universidad Miguel Hernández de Elche.  
  [https://hdl.handle.net/11000/28290](https://hdl.handle.net/11000/28290)
