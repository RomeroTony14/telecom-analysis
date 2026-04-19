# telecom-analysis# 📊 ConnectaTel - Análisis de Comportamiento de Clientes

## 🎯 Objetivo del Proyecto

El objetivo de este proyecto es analizar el comportamiento de los clientes de ConnectaTel en Latinoamérica, utilizando datos de uso de servicios móviles (llamadas y mensajes), información demográfica y planes contratados.

Se busca:
- Identificar patrones de uso
- Detectar comportamientos atípicos (outliers)
- Segmentar clientes según su nivel de uso y edad
- Generar insights accionables para mejorar la oferta comercial

---

## 📂 Datasets Utilizados

El análisis se basa en tres fuentes de datos:

### 1. `plans.csv`
Contiene información sobre los planes disponibles:
- Precio
- Minutos incluidos
- GB incluidos
- Costos adicionales

### 2. `users_latam.csv`
Información de los usuarios:
- Edad (`age`)
- Ciudad (`city`)
- Fecha de registro (`reg_date`)
- Plan contratado (`plan`)
- Estado de churn

### 3. `usage.csv`
Registro del uso real:
- Tipo de evento (`type`: call / text)
- Duración de llamadas (`duration`)
- Longitud de mensajes (`length`)
- Fecha (`date`)
- Usuario (`user_id`)

---

## 🔄 Etapas del Análisis

El proyecto sigue un flujo estructurado de análisis:

### 1. Carga y Exploración
- Revisión de estructura (`.head()`, `.info()`, `.shape()`)

### 2. Validación de Calidad de Datos
- Detección de nulos
- Identificación de sentinels (-999, "?", etc.)
- Validación de fechas

### 3. Limpieza de Datos
- Imputación de valores inválidos
- Estandarización de categorías
- Corrección de fechas fuera de rango

### 4. Agregación de Datos
- Transformación de datos de uso a nivel usuario
- Creación de métricas:
  - Cantidad de llamadas
  - Cantidad de mensajes
  - Minutos totales

### 5. Análisis Exploratorio (EDA)
- Estadísticas descriptivas
- Histogramas
- Boxplots (detección de outliers)

### 6. Segmentación de Clientes
- Por nivel de uso (bajo, medio, alto)
- Por edad (joven, adulto, adulto mayor)

### 7. Insights de Negocio
- Identificación de heavy users
- Evaluación de segmentos
- Recomendaciones estratégicas

---

## ▶️ Cómo Ejecutar el Notebook

### Opción 1: GitHub (visualización)
1. Abre el repositorio en GitHub
2. Haz clic en el archivo `.ipynb`
3. Visualiza directamente el análisis

---

### Opción 2: Google Colab (recomendado para ejecución)

1. Ve a https://colab.research.google.com
2. Selecciona **"GitHub"**
3. Pega la URL de repositorio
4. Abre el notebook

O bien:
- Descarga el `.ipynb`
- Súbelo manualmente a Colab

---

### Opción 3: Local (Jupyter Notebook)

1. Instala dependencias:
```bash
pip install pandas numpy matplotlib seaborn

2. Ejecuta:
jupyter notebook
3. Abre el archivo .ipynb

🔁 Guía de Reproducción

Para reproducir el análisis:

Asegúrate de tener los datasets en la ruta:
/datasets/
Ejecuta el notebook en orden:
Carga de datos
Limpieza
Agregación
Análisis
Visualización
No ejecutes celdas fuera de orden (dependencias entre pasos)
💡 Conclusión General

El análisis revela que:

El consumo está concentrado en un grupo reducido de usuarios (heavy users)
Existen diferencias claras en comportamiento según nivel de uso
Los planes actuales pueden optimizarse mediante segmentación
🚀 Recomendaciones
Diseñar planes diferenciados por nivel de uso
Implementar estrategias de upselling
Monitorear usuarios intensivos como segmento clave
Activar usuarios de bajo uso para reducir churn

👨‍💻 Autor

Proyecto desarrollado como parte de formación en Data Analytics, aplicando principios de:

Análisis exploratorio (EDA)
Limpieza de datos
Segmentación

