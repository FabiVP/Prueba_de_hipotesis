# 📊 Proyecto de Pruebas de Hipótesis — Ingeniería de Sistemas

Este repositorio contiene el análisis estadístico de 4 hipótesis aplicadas a problemas de rendimiento, redes, cifrado y servidores, utilizando Python en Google Colab.

---

## 🧠 Objetivo

Evaluar diferentes hipótesis mediante pruebas estadísticas para validar diferencias y relaciones en datasets de ingeniería de sistemas.

---

## 📁 Estructura del Proyecto
hipotesis1_tstudent/
│── h1_tstudent.ipynb
│── tstudent_algoritmos.xlsx
│── H1_tstudent.png

hipotesis2_mannwhitney/
│── h2_mannwhitney.ipynb
│── mannwhitney_redes.xlsx
│── H2_mannwhitney.png

hipotesis3_anova/
│── h3_anova.ipynb
│── anova_cifrado.xlsx
│── H3_anova.png

hipotesis4_pearson/
│── h4_pearson.ipynb
│── correlacion_servidor.xlsx
│── H4_pearson.png

---

## 📌 Hipótesis Evaluadas

### 🔹 H1 — t-Student
- **Objetivo:** Comparar rendimiento entre dos algoritmos.
- **Prueba:** t-Student independiente (cola superior)
- **Variable:** operaciones por segundo

---

### 🔹 H2 — Mann-Whitney U
- **Objetivo:** Comparar latencia entre dos redes.
- **Prueba:** Mann-Whitney (cola inferior)
- **Variable:** tiempo en milisegundos

---

### 🔹 H3 — ANOVA
- **Objetivo:** Comparar tiempos de cifrado entre algoritmos.
- **Prueba:** ANOVA de una vía
- **Variable:** tiempo de cifrado (ms)

---

### 🔹 H4 — Correlación de Pearson
- **Objetivo:** Evaluar relación entre carga del servidor y tiempo de respuesta.
- **Prueba:** Pearson (cola superior)
- **Variable:** solicitudes vs tiempo de respuesta

---

## ⚙️ Tecnologías Utilizadas

- Python 3
- Google Colab
- Pandas
- NumPy
- SciPy
- Matplotlib

---

## 📊 Resultados Generales

En todas las hipótesis se obtuvo evidencia estadística suficiente para rechazar la hipótesis nula (H0), con valores p < 0.05.

Esto indica diferencias significativas o relaciones fuertes entre las variables analizadas.

---

## ▶️ Cómo ejecutar

1. Abrir cada notebook en Google Colab
2. Subir el archivo Excel correspondiente
3. Ejecutar todas las celdas en orden
4. Visualizar resultados y gráficos

---

## 📌 Autor

Proyecto académico — Ingeniería de Sistemas  
Análisis estadístico aplicado a problemas reales de computación y redes.

---

## 📎 Nota

Este proyecto fue desarrollado con fines educativos y de investigación estadística.