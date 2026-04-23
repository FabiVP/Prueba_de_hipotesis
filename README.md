# 📊 Prueba de Hipótesis — Ingeniería de Sistemas

**Autores:**  
- Chávez Apaza, Marcos Alberto  
- Villaverde, Fabiola Karina  

---

## 📌 Descripción del Proyecto

Este script realiza **cuatro pruebas de hipótesis estadísticas** aplicadas a problemas de Ingeniería de Sistemas:

| Hipótesis | Prueba Estadística | Problema de estudio |
|-----------|-------------------|---------------------|
| **H1** | t-Student (cola superior) | Comparación de rendimiento entre dos algoritmos (ops/seg) |
| **H2** | Mann-Whitney U (cola inferior) | Comparación de latencia entre dos redes (ms) |
| **H3** | ANOVA de una vía | Comparación de tres algoritmos de cifrado (AES-256, RSA-2048, ChaCha20) |
| **H4** | Correlación de Pearson (cola superior) | Relación entre solicitudes concurrentes y tiempo de respuesta del servidor |

Cada análisis incluye:
- Estadísticas descriptivas
- Verificación de supuestos (normalidad, homogeneidad de varianzas)
- Aplicación de la prueba estadística correspondiente
- Visualización de resultados (histogramas, boxplots, gráficos de dispersión)
- Resumen ejecutivo con decisión estadística

---

## 📁 Archivos necesarios

Antes de ejecutar el script, asegúrate de tener los siguientes archivos `.xlsx`:

| Archivo | Descripción | Columnas requeridas |
|---------|-------------|---------------------|
| `tstudent_algoritmos.xlsx` | Datos para H1 | `Algoritmo_A_ops_sec`, `Algoritmo_B_ops_sec` |
| `mannwhitney_redes.xlsx` | Datos para H2 | `Red_X_ms`, `Red_Y_ms` |
| `anova_cifrado.xlsx` | Datos para H3 | `AES_256`, `RSA_2048`, `ChaCha20` |
| `correlacion_servidor.xlsx` | Datos para H4 | `Solicitudes_Concurrentes`, `Tiempo_Respuesta_ms` |

---

## 🚀 Instrucciones para ejecutar en Google Colab

### 1️⃣ Abrir Google Colab

Ve a [https://colab.research.google.com](https://colab.research.google.com)

### 2️⃣ Crear un nuevo Notebook

Haz clic en **"Nuevo Notebook"** (o Archivo → Nuevo notebook)

### 3️⃣ Copiar el script completo

Copia **todo el código** proporcionado (las 4 hipótesis completas) y pégalo en una **celda de código** del notebook.

> ⚠️ **Importante:** El script completo debe ejecutarse en UNA SOLA CELDA para que funcione correctamente la carga secuencial de archivos.

### 4️⃣ Ejecutar la celda

Presiona `Shift + Enter` o haz clic en el botón de reproducción ▶️ en la celda.

### 5️⃣ Subir los archivos cuando se solicite

El script te pedirá que subas los archivos **en orden**. Sigue estas indicaciones:

| Paso | Mensaje en Colab | Archivo a subir |
|------|------------------|-----------------|
| 1 | `📂 Sube el archivo: tstudent_algoritmos.xlsx` | `tstudent_algoritmos.xlsx` |
| 2 | `📂 Sube el archivo: mannwhitney_redes.xlsx` | `mannwhitney_redes.xlsx` |
| 3 | `📂 Sube el archivo: anova_cifrado.xlsx` | `anova_cifrado.xlsx` |
| 4 | `📂 Sube el archivo: correlacion_servidor.xlsx` | `correlacion_servidor.xlsx` |

**Para cada solicitud:**
1. Haz clic en el botón **"Elegir archivos"**
2. Selecciona el archivo correspondiente desde tu computadora
3. Espera a que termine la carga
4. El script continuará automáticamente al siguiente paso

### 6️⃣ Esperar los resultados

El script ejecutará las 4 pruebas secuencialmente. Para cada hipótesis verás:
- Tablas de estadísticas descriptivas
- Verificación de supuestos (Shapiro-Wilk, Levene)
- Resultado de la prueba (estadístico, p-valor, decisión)
- Gráficos generados automáticamente
- Resumen ejecutivo

### 7️⃣ Descargar los gráficos (opcional)

Los gráficos se guardan automáticamente como:
- `H1_tstudent.png`
- `H2_mannwhitney.png`
- `H3_anova.png`
- `H4_pearson.png`

Para descargarlos:
1. Haz clic en el icono de carpeta 📁 en el panel izquierdo de Colab
2. Navega por los archivos generados
3. Haz clic derecho sobre la imagen y selecciona "Descargar"

---

## 📊 Estructura de los archivos de datos

### `tstudent_algoritmos.xlsx`
| Algoritmo_A_ops_sec | Algoritmo_B_ops_sec |
|---------------------|---------------------|
| 125.3 | 98.7 |
| 132.1 | 101.2 |
| ... | ... |

### `mannwhitney_redes.xlsx`
| Red_X_ms | Red_Y_ms |
|----------|----------|
| 45.2 | 67.8 |
| 48.1 | 72.3 |
| ... | ... |

### `anova_cifrado.xlsx`
| AES_256 | RSA_2048 | ChaCha20 |
|---------|----------|----------|
| 12.5 | 45.2 | 10.3 |
| 13.1 | 47.8 | 11.2 |
| ... | ... | ... |

### `correlacion_servidor.xlsx`
| Solicitudes_Concurrentes | Tiempo_Respuesta_ms |
|--------------------------|---------------------|
| 10 | 85 |
| 20 | 120 |
| ... | ... |

---

## 📈 Resultados esperados

### H1: t-Student
- **Decisión esperada:** Rechazar H0 ✅
- **Conclusión:** El Algoritmo A es significativamente más rápido que el Algoritmo B

### H2: Mann-Whitney
- **Decisión esperada:** Rechazar H0 ✅
- **Conclusión:** La Red X presenta latencias significativamente menores que la Red Y

### H3: ANOVA
- **Decisión esperada:** Rechazar H0 ✅
- **Conclusión:** Al menos un algoritmo de cifrado tiene tiempo de procesamiento diferente
- **Post-hoc Tukey:** Identifica qué pares de algoritmos difieren significativamente

### H4: Correlación de Pearson
- **Decisión esperada:** Rechazar H0 ✅
- **Conclusión:** Existe una correlación positiva fuerte entre solicitudes concurrentes y tiempo de respuesta

---

## ❓ Solución de problemas comunes

| Problema | Posible causa | Solución |
|----------|---------------|----------|
| `FileNotFoundError` | Archivo no subido o nombre incorrecto | Verifica que subiste el archivo exactamente con el nombre solicitado |
| `KeyError: 'Nombre_Columna'` | Nombre de columna incorrecto | Revisa que los nombres en el Excel coincidan exactamente con los esperados |
| El script se detiene después de subir un archivo | Error en el archivo | Verifica que el archivo sea `.xlsx` válido y contenga datos numéricos |
| `NameError: name 'files' is not defined` | Código ejecutado fuera de Colab | Asegúrate de ejecutar el script dentro de Google Colab |
| Los gráficos no se muestran | Entorno sin interfaz gráfica | En Colab se muestran automáticamente debajo de la celda |
| `No module named 'scipy'` | Dependencia faltante | Ejecuta `!pip install scipy` antes del script (aunque Colab ya lo incluye) |

---

## 📝 Notas adicionales

- **Nivel de significancia:** Todas las pruebas usan α = 0.05
- **Pruebas unilaterales:** H1 (cola superior), H2 (cola inferior), H4 (cola superior)
- **Prueba bilateral:** H3 (ANOVA)
- **Post-hoc:** Para ANOVA se incluye automáticamente la prueba de Tukey HSD
- **Robustez:** H2 usa Mann-Whitney (no paramétrica) adecuada para datos de latencia
- **Normalidad:** Todas las pruebas verifican supuestos previamente

---

## 📄 Licencia

Este proyecto es de uso académico para la materia de **Ingeniería de Sistemas**.

---