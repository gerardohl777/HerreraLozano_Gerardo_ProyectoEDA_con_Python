# 📊 Proyecto Final Máster Data Analytics  
## Análisis Sintético de Jugadores de Fútbol  

### 🎯 Objetivo del proyecto
Este proyecto es el **Trabajo Final** del Máster en Data Analytics.  
El objetivo es aplicar todas las competencias aprendidas en el programa sobre un **dataset sintético de fútbol**, incluyendo:

- Limpieza y transformación de datos.  
- Análisis exploratorio (EDA).  
- Análisis estadístico.  
- Visualización de datos.  
- Creación de un **dashboard interactivo** en Power BI.  
- Documentación del proceso y resultados.  

---

## 📂 Estructura del repositorio

Proyecto_Final_Futbol/
│
├── data/
│ ├── raw/ # Datos en bruto (contratos + estadísticas de partidos)
│ │ ├── contratos_jugadores_raw.csv
│ │ └── estadisticas_partidos_raw.csv
│ │
│ ├── processed/ # Datos procesados
│ │ ├── jugadores_final.csv # Dataset final unificado y enriquecido
│ │ └── exports/ # Archivos preparados para dashboard
│ │ ├── jugadores_temporada.csv
│ │ ├── equipos_temporada.csv
│ │ ├── posiciones_temporada.csv
│ │ └── muestra_detalle_partidos.csv
│
├── notebooks/ # Jupyter Notebooks (Python + Pandas)
│ ├── 01_Generar_Dataset_Futbol.ipynb
│ ├── 02_EDA.ipynb
│ ├── 03_Estadistica.ipynb
│ └── 04_Export_Dashboard.ipynb
│
├── reports/
│ └── figures/ # Figuras generadas en el EDA



---

## ⚙️ Herramientas utilizadas

- **Python (Pandas, Matplotlib, Seaborn, Scipy)** → limpieza, análisis y estadísticas.  
- **Jupyter Notebooks** → desarrollo del análisis.  
- **Power BI Desktop (versión gratuita)** → visualización interactiva y dashboard final.  

---

## 📑 Proceso del proyecto

### 1️⃣ Generación y preparación de datos
- Se crean dos datasets sintéticos:
  - **Contratos de jugadores** (edad, altura, peso, salario, equipo, pie preferido, etc.).  
  - **Estadísticas de partidos** (goles, asistencias, minutos, tiros, pases, xG, xA, tarjetas, etc.).  
- Se integran en un **dataset final (`jugadores_final.csv`)** con más de **60.000 registros y >20 columnas**.  
- Se calculan métricas derivadas:
  - **IMC (índice de masa corporal)**.  
  - **Contribuciones** = goles + asistencias.  
  - Métricas **por 90 minutos** (goles, asistencias, contribuciones, xG, xA).  
  - Salario convertido a **millones de euros**.

---

### 2️⃣ Análisis exploratorio (EDA)
- Histogramas de distribución (minutos jugados, goles, asistencias, salarios, IMC).  
- Boxplots por posición (`DEF`, `MID`, `FWD`, `GK`) para comparar rendimiento.  
- Matriz de correlación entre variables numéricas.  
- Conclusiones:
  - Los delanteros concentran mayor contribución por 90’.  
  - La media de salario está correlacionada con la posición y contribución.  
  - Se observa una ligera caída de rendimiento con la edad.

---

### 3️⃣ Análisis estadístico
- **ANOVA**: contribuciones por 90’ varían significativamente según la posición.  
- **Correlación Pearson**: edad y contribuciones por 90’ tienen correlación negativa ligera.  
- **t-test**: no se encuentran diferencias significativas en contribución entre jugadores zurdos y diestros.  

---

### 4️⃣ Exportación para dashboard
Se generan 4 archivos listos para Power BI en formato europeo (`;` como separador y `,` como decimal):

- `jugadores_temporada.csv` → métricas agregadas por jugador y temporada.  
- `equipos_temporada.csv` → totales por equipo y temporada.  
- `posiciones_temporada.csv` → totales por posición y temporada.  
- `muestra_detalle_partidos.csv` → muestra aleatoria de 60.000 registros para detalle.  

---

## 📊 Dashboard en Power BI

El dashboard se compone de varias páginas:

### 🔹 Página 1 – Visión general
- Tarjetas (KPIs): goles totales, asistencias, contribuciones, contribuciones por 90’, salario medio.  

### 🔹 Página 2 – Comparativas
- **Gráfico de barras**: contribuciones por posición.  
- **Líneas**: evolución de goles por temporada y equipo.  

### 🔹 Página 3 – Detalle jugadores
- **Tabla** con: nombre, equipo, posición, goles, asistencias, contribuciones/90, salario.  
- **Segmentadores**: temporada, equipo, posición.  

### 🔹 Página 4 – Análisis avanzado
- **Dispersión**: salario vs contribuciones por 90’ (tamaño = minutos, color = posición).  
- **Gráfico circular**: distribución de jugadores por nacionalidad.  

---

## 📌 Conclusiones
- El dataset demuestra cómo unir datos contractuales y de rendimiento permite obtener insights valiosos.  
- Los delanteros tienen mayor impacto en contribuciones, pero también los salarios más altos.  
- Existe una tendencia decreciente en el rendimiento con la edad, aunque no es muy marcada.  
- Power BI permite explorar fácilmente relaciones entre salario, posición y rendimiento.  

---

✍️ **Autor**: [Gerardo Herrera Lozano]  
