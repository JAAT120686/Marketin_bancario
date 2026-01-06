
[Marketing Bancario](Unknown.png)

# 🏦 Proyecto: Marketing Bancario (Bank Marketing)

<br>
Este proyecto analiza datos de campañas telefónicas de un banco para predecir si un cliente suscribirá un depósito a plazo y así **optimizar el contacto comercial**.

---

## 🚀 Objetivo
Implementar análisis de datos y un modelo baseline de clasificación para **reducir llamadas inútiles** y mejorar la eficiencia de la campaña.

---

## 🧩 Estructura del Proyecto
- `Marketin_bancario.ipynb`: análisis exploratorio (EDA), preprocesamiento, modelado y evaluación
- `bank-additional-full.csv`: dataset completo (separador `;`)
- `bank-additional.csv`: versión reducida del dataset
- `bank-additional-names.txt`: descripción de variables
- `scripts/eda.py`: EDA rápido por script (opcional)
- `requirements.txt`: dependencias

---

## 🛠️ Tecnologías y Herramientas
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" height="24"> <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" height="24"> <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" height="24"> <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" height="24"> <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white" height="24"> <img src="https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge" height="24">

---

## 📦 Instalación (entorno)

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

---

## ▶️ Ejecución

### Notebook (recomendado)
1) Abre `Marketin_bancario.ipynb` en VS Code.
2) Selecciona el kernel del entorno `.venv`.
3) Ejecuta las celdas en orden.

### Script (opcional)
```bash
python scripts/eda.py
```

---

## 📈 Resultados Destacados
- El target `y` está **desbalanceado**, por lo que se priorizan métricas como **PR-AUC** y análisis por umbral.
- Se entrena un baseline con **Regresión Logística + OneHotEncoder** y `class_weight="balanced"`.
- Se realiza **split temporal 80/20** para evaluación más realista.
- Se analiza el trade-off **precision vs recall** para ajustar el umbral cuando el objetivo es **evitar llamadas inútiles**.

Notas metodológicas clave:
- Se excluye `duration` del modelado por **fuga de información** (no está disponible antes de la llamada).

---

## 🖼️ Visualización

### Ejemplo de resultado
![Ejemplo de salida/curva](output.png)

---

## 🏁 Conclusión del Proyecto

Este proyecto muestra cómo el análisis exploratorio y un modelo baseline pueden apoyar decisiones comerciales en campañas de marketing bancario. En particular, el ajuste de umbral permite alinear el modelo con el objetivo operativo de **reducir llamadas con baja probabilidad de conversión**, sin dejar de medir el impacto sobre la detección de clientes potenciales.

